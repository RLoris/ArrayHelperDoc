# ArrayHelper

![thumbnail](./assets/thumbnail.png)

- UE Plugin to handle arrays operations (sort, filter, match, range, clamp, random, average, min, max, normalize)
- Use custom predicate function to sort or filter arrays (Int, Float, Byte, Integer64, String, Name, Vector, Object, Actor, Generic)
- This is a blueprint library plugin
- It exposes 60+ functions to handle arrays by value or by reference
- Can be used in any blueprint

<br>

![Nodes](./assets/nodes.png)

[Link to the plugin in marketplace](https://www.unrealengine.com/marketplace/en-US/product/array-helper-bp-library)

<br>

# Documentation

<br>

# Average

![Average](./assets/average.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| AverageInteger | Array(Integer) | Average(Float) | Computes the average of an array |
| AverageFloat | Array(Float) | Average(Float) | Computes the average of an array |
| AverageByte | Array(Byte) | Average(Byte) | Computes the average of an array |
| AverageInteger64 | Array(Integer64) | Average(Integer64) | Computes the average of an array |

<br>

# Minimum

![Minimum](./assets/min.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| MinimumIntegerIndex | Array(Integer) | Index(Integer) | Returns the index of the minimum value in the array or -1 |
| MinimumFloatIndex | Array(Float) | Index(Integer) | Returns the index of the minimum value in the array or -1 |
| MinimumByteIndex | Array(Byte) | Index(Byte) | Returns the index of the minimum value in the array or -1 |
| MinimumInteger64Index | Array(Integer64) | Index(Integer64) | Returns the index of the minimum value in the array or -1 |

<br>

# Maximum

![Maximum](./assets/max.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| MaximumIntegerIndex | Array(Integer) | Index(Integer) | Returns the index of the maximum value in the array or -1 |
| MaximumFloatIndex | Array(Float) | Index(Integer) | Returns the index of the maximum value in the array or -1 |
| MaximumByteIndex | Array(Byte) | Index(Byte) | Returns the index of the maximum value in the array or -1 |
| MaximumInteger64Index | Array(Integer64) | Index(Integer64) | Returns the index of the maximum value in the array or -1 |

<br>

# Normalization

![Normalization](./assets/normalization.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| MinMaxFloatNormalization | Array(Float), Min(Float), Max(Float) | Array(Float) | Normalize the value of the array between min and max |
| MinMaxIntegerNormalization | Array(Integer), Min(Integer), Max(Integer) | Array(Integer) | Normalize the value of the array between min and max |
| MinMaxByteNormalization | Array(Byte), Min(Byte), Max(Byte) | Array(Byte) | Normalize the value of the array between min and max |
| MinMaxInteger64Normalization | Array(Integer64), Min(Integer64), Max(Integer64) | Array(Integer64) | Normalize the value of the array between min and max |

<br>

# Reverse (by copy)

![Reverse](./assets/reverse.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ReverseArray | Array(*) | Array(*) | Reverse a generic array by copy and return the reversed array |

<br>

# Convert

![Convert](./assets/convert.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| SplitString | String | Array(String) | Splits a string using a specific separator and return an array of strings |
| ToSet | Array(*) | Set(*) | Converts a generic array to a new set (removes duplicate) |
  
<br>

# Clamp

![Clamp](./assets/clamp.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ClampInteger | Array(Integer), Min, Max | Array(Integer) | Returns a new array clamped using min and max value |
| ClampFloat | Array(Float), Min, Max | Array(Float) | Returns a new array clamped using min and max value |
| ClampByte | Array(Byte), Min, Max | Array(Byte) | Returns a new array clamped using min and max value |
| ClampInteger64 | Array(Integer64), Min, Max | Array(Integer64) | Returns a new array clamped using min and max value |
| ClampVector | Array(Vector), MinSize, MaxSize, Only2D | Array(Vector) | Returns a new array clamped using min and max value |
| ClampIntegerByRef | Array(Integer), Min, Max | void | Updates the input array and clamp values using min and max value |
| ClampFloatByRef | Array(Float), Min, Max | void | Updates the input array and clamp values using min and max value |
| ClampByteByRef | Array(Byte), Min, Max | void | Updates the input array and clamp values using min and max value |
| ClampInteger64ByRef | Array(Integer64), Min, Max | void | Updates the input array and clamp values using min and max value |
| ClampVectorRef | Array(Vector), MinSize, MaxSize, Only2D | void | Updates the input array and clamp values using min and max value |

<br>

# Range

![Range](./assets/range.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ExtractArray | Array(*), StartIndex, EndIndex | Array(*) | Returns a subarray of the first generic array using start and end index |

<br>

# Random

![Random](./assets/random.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| RandomInteger | Size, Min, Max | Array(Integer) | Returns a random array filled with value between min and max |
| RandomFloat | Size, Min, Max | Array(Float) | Returns a random array filled with value between min and max |
| RandomVector | Size, Min, Max | Array(Vector) | Returns a random array filled with value between min and max |
| RandomByte | Size, Min, Max | Array(Byte) | Returns a random array filled with value between min and max |
| RandomBoolean | Size | Array(Boolean) | Returns a random array filled with value |
| RandomInteger64 | Size, Min, Max | Array(Integer64) | Returns a random array filled with value between min and max |
| PickRandomItem | Array(*), Weights(Int) | Item(*), Index(Int) | Picks a random item in a generic array based on weights and returns it with its index |

<br>

# Sort

![Sort](./assets/sort.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| SortInteger | Array(Integer), IsAscending | Array(Integer) | Returns a copy of the array sorted by descending or ascending order |
| SortFloat | Array(Float), IsAscending | Array(Float) | Returns a copy of the array sorted by descending or ascending order |
| SortByte | Array(Byte), IsAscending | Array(Byte) | Returns a copy of the array sorted by descending or ascending order |
| SortInteger64 | Array(Integer64), IsAscending | Array(Integer64) | Returns a copy of the array sorted by descending or ascending order |
| SortString | Array(String), IsAscending | Array(String) | Returns a copy of the array sorted by descending or ascending order |
| SortName | Array(Name), IsAscending | Array(Name) | Returns a copy of the array sorted by descending or ascending order |
| SortVector | Array(Vector), Origin(Vector), IsAscending | Array(Vector) | Returns a copy of the array sorted by descending or ascending order based on Origin |
| SortActor | Array(Actor), Origin(Actor), isAscending | Array(Actor) | Returns a copy of the array sorted by descending or ascending order based on distance to origin |
| SortIntegerByRef | Array(Integer), IsAscending | void | Sorts the input array by descending or ascending order |
| SortFloatByRef | Array(Float), IsAscending | void | Sorts the input array by descending or ascending order |
| SortByteByRef | Array(Byte), IsAscending | void | Sorts the input array by descending or ascending order |
| SortInteger64ByRef | Array(Integer64), IsAscending | void | Sorts the input array by descending or ascending order |
| SortStringByRef | Array(String), IsAscending | void | Sorts the input array by descending or ascending order |
| SortNameByRef | Array(Name), IsAscending | void | Sorts the input array by descending or ascending order |
| SortVectorByRef | Array(Vector), Origin, IsAscending | void | Sorts the input array by descending or ascending order based on Origin |
| SortActorByRef | Array(Actor), Origin(Actor), IsAscending | void | Sorts the input array by descending or ascending order based on distance to origin |

<br>

# Sort by predicate

![Predicate Sort](./assets/predicate_sort.png)
 
    Note v2: In order to sort by predicate you must create a functions by dragging the PredicateFunction pin and select create event, then create or select a matching function in the list

    Note v1.1 and minor: In order to sort by predicate you must implement the ArrayComparator Interface and pass the object implementing this interface as input of the function (Context), the appropriate compare method will be called to perform the sort

![Example Sort](./assets/predicate_sort_delegate.png)
![Example Sort](./assets/predicate_sort_function.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| PredicateSortInteger | Array(Integer), PredicateFunction, InvertResult | Array(Integer) | Returns a new array sorted using a custom predicate |
| PredicateSortFloat | Array(Float), PredicateFunction, InvertResult | Array(Float) | Returns a new array sorted using a custom predicate |
| PredicateSortByte | Array(Byte), PredicateFunction, InvertResult | Array(Byte) | Returns a new array sorted using a custom predicate |
| PredicateSortInteger64 | Array(Integer64), PredicateFunction, InvertResult | Array(Integer64) | Returns a new array sorted using a custom predicate |
| PredicateSortString | Array(String), PredicateFunction, InvertResult | Array(String) | Returns a new array sorted using a custom predicate |
| PredicateSortName | Array(Name), PredicateFunction, InvertResult | Array(Name) | Returns a new array sorted using a custom predicate |
| PredicateSortVector | Array(Vector),PredicateFunction, InvertResult | Array(Vector) | Returns a new array sorted using a custom predicate |
| PredicateSortObject | Array(Object), PredicateFunction, InvertResult | Array(Object) | Returns a new array sorted using a custom predicate |
| PredicateSortActor | Array(Actor), PredicateFunction, InvertResult | Array(Actor) | Returns a new array sorted using a custom predicate |
| PredicateSortIntegerByRef | Array(Integer), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortFloatByRef | Array(Float), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortByteByRef | Array(Byte), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortInteger64ByRef | Array(Integer64), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortStringByRef | Array(String), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortNameByRef | Array(Name), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortVectorByRef | Array(Vector), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortObjectByRef | Array(Object), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |
| PredicateSortActorByRef | Array(Actor), PredicateFunction, InvertResult | void | Sorts the input array using a custom predicate |

<br>

# Distance

![Distance](./assets/vector.png)
 
| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| ClosestLocation | Array(Vector), Origin(Vector) | Closest(Vector), Distance, Index | Return the closest vector to Origin, the distance, the index in array |
| FarthestLocation | Array(Vector), Origin(Vector) | Farthest(Vector), Distance, Index | Return the farthest vector to Origin, the distance, the index in array |
| ClosestActor | Array(Actor), Origin(Actor) | Closest(Actor), Distance, Index | Return the closest actor to Origin, the distance, the index in array |
| FarthestActor | Array(Actor), Origin(Actor) | Farthest(Actor), Distance, Index | Return the farthest actor to Origin, the distance, the index in array |

<br>

# Filters

![Filter](./assets/filter.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| FilterMatches | Array(String), Pattern | Found, Array(String) | Returns an array containing strings that match the pattern (regex) |
| FilterMatch | Array(String), Pattern | Found, String, Index | Returns the first string matching the pattern (regex) with its index |

<br>

# Filters by predicate

![Predicate Filter](./assets/predicate_filter.png)

    Note v2: In order to filter by predicate you must create a functions by dragging the PredicateFunction pin and select create event, then create or select a matching function in the list

    Note v1.1 and minor : In order to filter by predicate you must implement the ArrayFilter Interface and pass the object implementing this interface as input of the function (Context), the appropriate filter method will be called to perform the filtering

![Example Filter](./assets/predicate_filter_delegate.png)
![Example Filter](./assets/predicate_filter_function.png)

| Node | Inputs | Outputs | Note |
| -------- | ---- | ---- | ---- |
| PredicateFilterInteger | Array(Integer), PredicateFunction, InvertResult | Array(Integer) | Returns a new array filtered using a custom predicate |
| PredicateFilterFloat | Array(Float), PredicateFunction, InvertResult | Array(Float) | Returns a new array filtered using a custom predicate |
| PredicateFilterByte | Array(Byte), PredicateFunction, InvertResult | Array(Byte) | Returns a new array filtered using a custom predicate |
| PredicateFilterInteger64 | Array(Integer64), PredicateFunction, InvertResult | Array(Integer64) | Returns a new array filtered using a custom predicate |
| PredicateFilterString | Array(String), PredicateFunction, InvertResult | Array(String) | Returns a new array filtered using a custom predicate |
| PredicateFilterName | Array(Name), PredicateFunction, InvertResult | Array(Name) | Returns a new array filtered using a custom predicate |
| PredicateFilterVector | Array(Vector), PredicateFunction | Array(Vector) | Returns a new array filtered using a custom predicate, InvertResult |
| PredicateFilterObject | Array(Object), PredicateFunction | Array(Object) | Returns a new array filtered using a custom predicate, InvertResult |
| PredicateFilterActor | Array(Actor), PredicateFunction | Array(Actor) | Returns a new array filtered using a custom predicate, InvertResult |

 
 
