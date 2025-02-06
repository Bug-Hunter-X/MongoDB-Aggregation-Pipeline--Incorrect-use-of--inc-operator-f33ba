# MongoDB Aggregation Pipeline: Incorrect use of $inc operator
This repository demonstrates a common error when using the MongoDB aggregation pipeline: incorrectly using the `$inc` operator.  The `$inc` operator is for modifying documents, not for calculations within the aggregation pipeline.  This example shows the incorrect usage and provides a corrected version.

## Problem
The provided `bug.js` file contains code that attempts to increment the `count` field using `$inc` within the aggregation pipeline. This is invalid and will throw an error.  The `$inc` operator is used for updating documents, not for processing and transforming data within an aggregation pipeline.

## Solution
The `bugSolution.js` file provides the correct approach using the `$add` operator to add 1 to the existing count in the aggregation pipeline, and this should be used before the $limit stage to ensure all values are summed correctly.