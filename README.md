# React Native: TypeError: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common error in React Native applications: the `TypeError: Cannot read properties of undefined (reading 'name')` exception.  This error typically arises when attempting to access a property of an object that is currently `undefined` or `null`.  The example provided shows how this can occur during asynchronous data fetching.

## Problem Description

The issue lies in accessing the `user.name` property before the `fetchUser()` function completes and sets the `user` state. If the `fetchUser()` function is slow or has encountered an error and hasn't set the `user` state to a proper object with a `name` property, trying to access `user.name` results in the error.

## Solution

The solution is to implement a check for the `user` object's existence and validity before attempting to access its properties.
