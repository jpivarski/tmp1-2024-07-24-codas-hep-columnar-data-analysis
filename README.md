# CoDaS-HEP 2024 Columnar Data Analysis Tutorial

[![Binder](https://binderhub.ssl-hep.org/badge_logo.svg)](https://binderhub.ssl-hep.org/v2/gh/ianna/2024-07-24-codas-hep-columnar-data-analysis.git/HEAD)

**Abstract:**

Data analysis languages like Numpy, MATLAB, R, IDL, ADL, and Julia are primarily interactive, using an array-at-a-time interface. Instead of conducting an entire analysis in a single loop, each calculation step is performed separately, allowing users to inspect distributions at each stage.

However, these languages are typically limited to primitive data types, such as numbers and booleans. Variable-length and nested data structures, like varying numbers of particles per event, don’t fit well into this model. Fortunately, this limitation can be overcome.

In this tutorial, we will introduce awkward-array, explore the concepts of columnar data structures, and demonstrate how to leverage them in data analysis. For example, we’ll show how to compute combinatorics (quantities depending on combinations of particles) without using any for loops.

