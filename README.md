# React Native AsyncStorage: Handling Non-String Data

This repository demonstrates a common issue in React Native when using AsyncStorage: attempting to store non-string data.  AsyncStorage only supports string values. Storing other data types (objects, numbers, etc.) will lead to data loss or unexpected app behavior.  The provided code examples showcase the problem and its solution.

## Problem

The `bug.js` file illustrates the incorrect approach, trying to store a JavaScript object in AsyncStorage.

## Solution

The `bugSolution.js` file demonstrates how to properly store data in AsyncStorage by first converting it to a string using `JSON.stringify`.  Data retrieval involves parsing the string back into its original object using `JSON.parse`.