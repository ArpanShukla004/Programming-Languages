# Introduction

## What is Data ?

- Data is any piece of information that a computer can store and process.
- It can represent numbers, text, images, or any kind of value used by a program.
- For example, a student's name, age, and marks are all forms of data.
- Programs use data to perform calculations, make decisions, and produce results.
- In simple terms, data is the raw information that a program works with.

## What is Data Structure ?

A data structure is a way of organizing and storing data so that it can be used efficiently. When programs handle large amounts of data, they need a proper structure to manage it. Data structures help in accessing, modifying, and managing data easily. Different data structures are designed for different types of operations. In simple terms, a data structure defines how data is arranged and used in a program.

## Why Data Structures are needed ?

- Programs often work with large amounts of data, not just single values.
- Without proper organization, managing and processing this data becomes difficult.
- Data structures help store and organize data efficiently.
- They make operations like searching, inserting, and deleting data faster.
- In simple terms, data structures help programs manage data in an efficient and structured way.

## Types of Data Structures

- Data Structures are mainly classified into two types : Linear and Non - Linear.

### 1. Linear Data Structures : 

- A linear data structure stores elements in a sequential order, one after another.
- Each element is connected to its previous and next element in a single line.
- This creates a clear, step-by-step traversal from the first element to the last.
- Operations like insertion, deletion, and traversal usually follow this sequence.
- Common examples include Arrays, Linked Lists, Stacks, and Queues.

### 2. Non - Linear Data Structures : 

- A non-linear data structure stores elements in a hierarchical or network-like structure.
- Elements are not arranged in a single sequence.
- One element can be connected to multiple other elements.
- This allows representation of more complex relationships between data.
- Common examples include Trees and Graphs.

## Basic Operations in Data Structures : 

- Data structures allow programs to store, access, and modify data efficiently. To manage the stored data, certain common actions are performed. These actions are called basic operations.

- Understanding these operations helps us know how a data structure behaves when data changes.

- The most common operations are :

### 1. Insertion : 
Insertion means adding a new element to the data structure.
The element may be inserted:
-> at the beginning
-> in the middle
-> at the end

**Example:**
If we have an array:
```bash 
[10, 20, 30]
```
After inserting **40** at the end:

```bash
[10, 20, 30, 40]
```

- Insertion is important when new data needs to be stored in a program.

### 2. Deletion : 
Deletion means removing an existing element from the data structure.

**Example:**
```bash 
[10, 20, 30, 40]
```

After deleting **20**:

```bash
[10, 30, 40]
```

- Deletion is used when data is no longer needed.

### 3. Searching :
Searching means finding a specific element inside a data structure.

**Example:**
Searching for 30 in:
```bash
[10, 20, 30, 40]
```
- The program checks elements until it finds the required value.
- Searching is important when we need to retrieve particular information.

### 4. Traversal : 
Traversal means visiting each element of a data structure one by one.

**Example:**
For the array:
```bash
[10, 20, 30, 40]
```
Traversal would access elements in order:
```bash
10 → 20 → 30 → 40
```

- Traversal is commonly used when we need to process every element.

### 5. Updating :
Updating means modifying the value of an existing element.

**Example:**
```bash
[10, 20, 30]
```
Updating 20 to 25:
```bash
[10, 25, 30]
```

- This operation allows programs to change stored data when required.