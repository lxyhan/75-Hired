### LC1: Contains Duplicates (Easy)
Given a list of integers, return true if any value appears more than once. Return false otherwise.

##### Solution

```
def hasDuplicate(self, nums: List\[int]) -> bool:
    unique = set()
    for num in nums:
        unique.add(num)
    return len(nums) != len(unique)
```
**Explanation:** Sets cannot contain duplicate elements. If we add all elements from `nums` to a set, and the lengths differ, it means there was at least one duplicate.


##### Optimal Solution
```
def hasDuplicate(self, nums: List\[int]) -> bool:
    return len(nums) != len(set(nums))
````
**Explanation:** A pythonic way of solving this is to realize that the `set()` class takes an interable as a parameter and adds all the unique elements of that iterable to the set. This enables the more elegant code above, bypassing the need for a for loop. You can even construct a set with a string or dict as a parameter. `set(my_string)` would result in a set with all the unique characters in `my_string`; `set(my_dict)` would result in a set with all the unique keys in `my_dict`.

### 🔑 Takeaways:

* Sets are great for **checking duplicates** due to their uniqueness property

* Python's built-in data structures can simplify many algorithmic problems

* Always look for opportunities to **refactor loops into expressions**
