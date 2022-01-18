---
title: "Code Book"
author: "Austin Usselman"
date: "1/18/2022"
output: html_document
---

# run_analysis downloads and tidies data from http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

## Download the data
In folder UCI HAR Dataset

## Extract data for use
features from features.txt
activities from activity_labels.txt
subject_test from subject_test.txt
subject_train from subject_train.txt
x_test from X_test.txt
y_test from y_test.txt
x_train from X_train.txt
y_train from y_train.txt

## Merge Data
X is rbind(x_train, x_test)
Y is rbind(y_train, y_test)
Subject is rbind(subject_train, subject_test)
Merged is cbind(Subject, Y, X)

## Extracts mean and std for each measurement
TidyData is assigned the mean and std from the Merged data

## Labels
TidyData is labeled

# New data
FinalData is the average of each variable in TidyData and is outputted as TidyData.txt
