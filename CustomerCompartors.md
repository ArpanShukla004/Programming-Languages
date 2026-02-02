# Custom Comparator in C++

---

## What is a Comparator Function?

A comparator function is a **Boolean function** that takes **two arguments** and returns **true or false**.  

If it returns **true**, it means the **first element should come before the second** according to a given rule.  

It is used to **sort containers** like arrays, lists, and other linear data structures.

---

## How to Write a Comparator?

```cpp
bool Name_of_Comparator(DataType value1, DataType value2)
{
    if (/* criteria to decide order, e.g. value1 > value2 */)
    {
        return true;   // value1 comes before value2
    }
    else
    {
        return false;  // value1 does not come before value2
    }
}
```

---

## How to Use a Comparator?

In the `sort()` function, when you want to sort elements based on some other criteria that you have defined in your comparator, pass this comparator function as the third argument to `sort()`.

```cpp
sort(container.begin(), container.end(), comparator_name);
```

---

## Example: Sorting Strings by Length

```cpp
bool cmp(string a, string b)
{
    if (a.length() < b.length())
    {
        return true;
    }
    else
    {
        return false;
    }
}

vector<string> v = {"apple", "cat", "banana"};

sort(v.begin(), v.end(), cmp);
```

---

## Working of the Above Code

**Initial Vector:**
```
["apple", "cat", "banana"]
```

**Step 1:** 

Compare "apple" and "cat"

cmp("apple", "cat")

"apple" length = 5

"cat" length = 3

5 < 3 → false

"apple" should NOT come before "cat"
"cat" comes before "apple"

**Intermediate Order:**
```
["cat", "apple", "banana"]
```

**Step 2:** 

Compare "apple" and "banana"

cmp("apple", "banana")

"apple" length = 5

"banana" length = 6

5 < 6 → true

"apple" comes before "banana"

Order remains:
```
["cat", "apple", "banana"]
```

**Step 3:**

Compare "cat" and "banana"  
`cmp("cat", "banana")`  
"cat" length = 3  
"banana" length = 6  
3 < 6 → true  
"cat" comes before "banana"

**Final Sorted Vector:**
```
["cat", "apple", "banana"]
```


## Practical Use Case

**Fractional Knapsack Problem
Sorting items based on highest value per weight**



```
bool comparator(pair<int,int> v1, pair<int,int> v2)
{
    if (v1.first / (double)v1.second >
        v2.first / (double)v2.second)
    {
        return true;
    }
    return false;
}
vector<pair<int,int>> Value_and_Weight = {
    {100,20},
    {60,10},
    {100,50},
    {200,50}
};

sort(Value_and_Weight.begin(), Value_and_Weight.end(), comparator);
```

---

## Converting Comparators: Ascending to Descending

**Core Idea:** Reverse the comparison condition

**Example:**

**Ascending Order:**
```cpp
return a.length() < b.length();
```

**Descending Order:**
```cpp
return a.length() > b.length();
```
