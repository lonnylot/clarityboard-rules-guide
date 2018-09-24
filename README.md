# Introduction

This is the Rule Guide for [Clarityboard](https://www.clarityboard.com). Below we explain which rules are required when creating new reports using the [Clarityboard API](https://clarityboard.docs.apiary.io/#).

# Overview

Each report displays one chart:

1. timeline
1. percentage
1. summary

Each chart requires a specific set of rules, described below.

## Rule Descriptions

### Record Group

`type`: `record-group`

`value`: Report Group ID (ex.: 'd290f1ee-6c54-4b01-90e6-d701748f0851')

This is used to specify the Record Group that the chart is using for data. All the other rules _must_ be in this Record Group.

### Field

`type`: `field`

`value`: The [Javascript Dot Notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors#Dot_notation) inside the [Record Group](https://www.clarityboard.com/records) data. (Ex: `Sale.Product.Name`)

### Sum

`type`: `sum`

`value`: The [Javascript Dot Notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors#Dot_notation) inside the [Record Group](https://www.clarityboard.com/records) data. (Ex: `Sale.Price`)

### Date Constraint

`type`: `date-constraint`

`value`: The [Javascript Dot Notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors#Dot_notation) inside the [Record Group](https://www.clarityboard.com/records) data. (Ex: `Sale.Sale-Date`)

We use this to select which records fall between a start and end date.

## Chart Requirements

### Timeline

The `timeline` chart **requires**:

1. record-group
1. date-constraint
1. field

### Percentage

The `percentage` chart **requires**:

1. record-group
1. date-constraint
1. field

### Summary

The `summary` chart **requires**:

1. record-group
1. date-constraint
1. field
1. sum
