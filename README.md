# Letter Combinations of a Phone Number

[![Java](https://img.shields.io/badge/Java-11%2B-orange.svg)](https://www.oracle.com/java/)
[![Problem Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow.svg)](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

An optimized Java solution for the classic **Letter Combinations of a Phone Number** problem, implemented using **Backtracking** (Depth-First Search).

---

## 📌 Problem Description

Given a string containing digits from `2-9` inclusive, return all possible letter combinations that the number could represent. Return the answer in **any order**.

A mapping of digits to letters (just like on standard telephone buttons) is shown below:

| Digit | Letters |
| :---: | :---: |
| **2** | `abc` |
| **3** | `def` |
| **4** | `ghi` |
| **5** | `jkl` |
| **6** | `mno` |
| **7** | `pqrs` |
| **8** | `tuv` |
| **9** | `wxyz` |

### Examples

**Example 1:**
* **Input:** `digits = "23"`
* **Output:** `["ad","ae","af","bd","be","bf","cd","ce","cf"]`

**Example 2:**
* **Input:** `digits = "2"`
* **Output:** `["a","b","c"]`

---

## 🚀 Approach & Algorithm

The problem is solved using a **Backtracking** approach:
1. **Mapping:** We maintain a pre-defined array (`PHONE_MAP`) mapping each digit (`2`-`9`) to its corresponding character set.
2. **DFS / Recursion:** We traverse through the input `digits` string index by index, building the combination character by character using a `StringBuilder` for high performance.
3. **Base Case:** When the length of the current combination matches the length of the input `digits`, we add the combination to our result list and backtrack.

---

## 📊 Complexity Analysis

* **Time Complexity:** $\mathcal{O}(4^N \cdot N)$, where $N$ is the length of the input `digits`. In the worst-case scenario (e.g., digits `7` or `9` which map to 4 letters), the branching factor is 4, and $N$ time is required to construct and copy strings into the final result list.
* **Space Complexity:** $\mathcal{O}(4^N \cdot N)$ to store the output results, alongside $\mathcal{O}(N)$ auxiliary space for the recursion call stack and `StringBuilder`.

---

## 🛠️ Getting Started

### Prerequisites
* Java Development Kit (**JDK 11** or higher recommended).

### Running the Code

1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/letter-combinations-phone-number.git](https://github.com/your-username/letter-combinations-phone-number.git)
