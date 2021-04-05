# ArrayHelper

- UE4 Plugin to handle arrays operations
- This is a blueprint library plugin
- It exposes 60 functions to handle arrays by value or by reference
- Can be used in any blueprint

![Nodes](./assets/nodes.png)

[Link to the plugin in marketplace](https://www.unrealengine.com/marketplace/en-US/product/array-helper-bp-library)

# Documentation

# Reverse (by copy)

![Reverse](./assets/reverse.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ReverseInteger | Array(Integer) | Array(Integer) | Reverse an array by copy and return the reversed array |
| ReverseFloat | Array(Float) | Array(Float) | Reverse an array by copy and return the reversed array |
| ReverseString | Array(String) | Array(String) | Reverse an array by copy and return the reversed array |
| ReverseName | Array(Name) | Array(Name) | Reverse an array by copy and return the reversed array |
| ReverseVector | Array(Vector) | Array(Vector) | Reverse an array by copy and return the reversed array |
| ReverseObject | Array(Object) | Array(Object) | Reverse an array by copy and return the reversed array |

# Convert

![Convert](./assets/convert.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| SplitString | String | Array(String) | Splits a string using a specific separator and return an array of strings |
| ToIntegerSet | Array(Integer) | Set(Integer) | Converts an array to a new set (removes duplicate) |
| ToFloatSet | Array(Float) | Set(Float) | Converts an array to a new set (removes duplicate) |
| ToNameSet | Array(Name) | Set(Name) | Converts an array to a new set (removes duplicate) |
| ToStringSet | Array(String) | Set(String) | Converts an array to a new set (removes duplicate) |
| ToVectorSet | Array(Vector) | Set(Vector) | Converts an array to a new set (removes duplicate) |
| ToObjectSet | Array(Object) | Set(Object) | Converts an array to a new set (removes duplicate) |
  
# Clamp

![Clamp](./assets/clamp.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ClampInteger | Array(Integer), Min, Max | Array(Integer) | Returns a new array clamped using min and max value |
| ClampFloat | Array(Float), Min, Max | Array(Float) | Returns a new array clamped using min and max value |
| ClampVector | Array(Vector), MinSize, MaxSize, Only2D | Array(Vector) | Returns a new array clamped using min and max value |
| ClampIntegerByRef | Array(Integer), Min, Max | void | Updates the input array and clamp values using min and max value |
| ClampFloatByRef | Array(Float), Min, Max | void | Updates the input array and clamp values using min and max value |
| ClampVectorRef | Array(Vector), MinSize, MaxSize, Only2D | void | Updates the input array and clamp values using min and max value |
  
# Range

![Range](./assets/range.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ExtractInteger | Array(Integer), StartIndex, EndIndex | Array(Integer) | Returns a subarray of the first array using start and end index |
| ExtractFloat | Array(Float), StartIndex, EndIndex | Array(Float) | Returns a subarray of the first array using start and end index |
| ExtractString | Array(String), StartIndex, EndIndex | Array(String) | Returns a subarray of the first array using start and end index |
| ExtractName | Array(Name), StartIndex, EndIndex | Array(Name) | Returns a subarray of the first array using start and end index |
| ExtractVector | Array(Vector), StartIndex, EndIndex | Array(Vector) | Returns a subarray of the first array using start and end index |
| ExtractObject | Array(Object), StartIndex, EndIndex | Array(Object) | Returns a subarray of the first array using start and end index |
  
# Random

![Random](./assets/random.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| RandomInteger | Size, Min, Max | Array(Integer) | Returns a random array filled with value between min and max |
| RandomFloat | Size, Min, Max | Array(Float) | Returns a random array filled with value between min and max |
| RandomVector | Size, Min, Max | Array(Vector) | Returns a random array filled with value between min and max |
  
# Sort

![Sort](./assets/sort.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| SortInteger | Array(Integer), IsAscending | Array(Integer) | Returns a copy of the array sorted by descending or ascending order |
| SortFloat | Array(Float), IsAscending | Array(Float) | Returns a copy of the array sorted by descending or ascending order |
| SortString | Array(String), IsAscending | Array(String) | Returns a copy of the array sorted by descending or ascending order |
| SortName | Array(Name), IsAscending | Array(Name) | Returns a copy of the array sorted by descending or ascending order |
| SortVector | Array(Vector), Origin, IsAscending | Array(Vector) | Returns a copy of the array sorted by descending or ascending order based on Origin |
| SortIntegerByRef | Array(Integer), IsAscending | void | Sorts the input array by descending or ascending order |
| SortFloatByRef | Array(Float), IsAscending | void | Sorts the input array by descending or ascending order |
| SortStringByRef | Array(String), IsAscending | void | Sorts the input array by descending or ascending order |
| SortNameByRef | Array(Name), IsAscending | void | Sorts the input array by descending or ascending order |
| SortVectorByRef | Array(Vector), Origin, IsAscending | void | Sorts the input array by descending or ascending order based on Origin |

# Sort by predicate

![Predicate Sort](./assets/predicate_sort.png)
 
In order to sort by predicate you must implement the ArrayComparator Interface and pass the object implementing this interface as input of the function (Context), the appropriate compare method will be called to perform the sort
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| PredicateSortInteger | Array(Integer), Context | Array(Integer) | Returns a new array sorted using a custom predicate implemented in Context |
| PredicateSortFloat | Array(Float), Context | Array(Float) | Returns a new array sorted using a custom predicate implemented in Context |
| PredicateSortString | Array(String), Context | Array(String) | Returns a new array sorted using a custom predicate implemented in Context |
| PredicateSortName | Array(Name), Context | Array(Name) | Returns a new array sorted using a custom predicate implemented in Context |
| PredicateSortVector | Array(Vector), Context | Array(Vector) | Returns a new array sorted using a custom predicate implemented in Context |
| PredicateSortObject | Array(Object), Context | Array(Object) | Returns a new array sorted using a custom predicate implemented in Context |
| PredicateSortIntegerByRef | Array(Integer), Context | void | Sorts the input array using a custom predicate implemented in Context |
| PredicateSortFloatByRef | Array(Float), Context | void | Sorts the input array using a custom predicate implemented in Context |
| PredicateSortStringByRef | Array(String), Context | void | Sorts the input array using a custom predicate implemented in Context |
| PredicateSortNameByRef | Array(Name), Context | void | Sorts the input array using a custom predicate implemented in Context |
| PredicateSortVectorByRef | Array(Vector), Context | void | Sorts the input array using a custom predicate implemented in Context |
| PredicateSortObjectByRef | Array(Object), Context | void | Sorts the input array using a custom predicate implemented in Context |
  
# Vectors

![Vector](./assets/vector.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ClosestLocation | Array(Vector), Origin | Closest, Distance, Index | Return the closest vector to Origin, the distance, the index in array |
| FarthestLocation | Array(Vector), Origin | Farthest, Distance, Index | Return the farthest vector to Origin, the distance, the index in array |
 
# Filters

![Filter](./assets/filter.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| FilterMatches | Array(String), Pattern | Found, Array(String) | Returns an array containing strings that match the pattern (regex) |
| FilterMatch | Array(String), Pattern | Found, String, Index | Returns the first string matching the pattern (regex) with its index |
 
# Filters by predicate

![Predicate Filter](./assets/predicate_filter.png)

In order to filter by predicate you must implement the ArrayFilter Interface and pass the object implementing this interface as input of the function (Context), the appropriate filter method will be called to perform the filtering

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| PredicateFilterInteger | Array(Integer), Context | Array(Integer) | Returns a new array filtered using a custom predicate implemented in Context |
| PredicateFilterFloat | Array(Float), Context | Array(Float) | Returns a new array filtered using a custom predicate implemented in Context |
| PredicateFilterString | Array(String), Context | Array(String) | Returns a new array filtered using a custom predicate implemented in Context |
| PredicateFilterName | Array(Name), Context | Array(Name) | Returns a new array filtered using a custom predicate implemented in Context |
| PredicateFilterVector | Array(Vector), Context | Array(Vector) | Returns a new array filtered using a custom predicate implemented in Context |
| PredicateFilterObject | Array(Object), Context | Array(Object) | Returns a new array filtered using a custom predicate implemented in Context |

 
 
