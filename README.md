# LEETCODE-Arrays-1980
### **Understanding the Algorithm:**
- The input is an array of binary strings, `nums`, each of length `n`.
- The function constructs a new binary string of length `n` using the following rule:
  - At index `i`, it flips the `i-th` character of `nums[i]` (i.e., if it's '1', it becomes '0', and vice versa).
- The output is the new binary string.

This approach is known as the **diagonal flipping method** and guarantees that the result is different from all the given strings.

---

### **Example 1**
#### **Input:**
```java
nums = ["01", "10"]
```
#### **Step-by-Step Execution:**
1. `n = nums.length = 2`
2. Initialize `sb = ""`
3. Loop through `i = 0` to `1`:
   - `i = 0`: `nums[0].charAt(0) = '0'`, flip → `'1'`, `sb = "1"`
   - `i = 1`: `nums[1].charAt(1) = '0'`, flip → `'1'`, `sb = "11"`
4. **Return "11"**

#### **Output:** `"11"`

---

### **Example 2**
#### **Input:**
```java
nums = ["000", "011", "111"]
```
#### **Step-by-Step Execution:**
1. `n = nums.length = 3`
2. Initialize `sb = ""`
3. Loop through `i = 0` to `2`:
   - `i = 0`: `nums[0].charAt(0) = '0'`, flip → `'1'`, `sb = "1"`
   - `i = 1`: `nums[1].charAt(1) = '1'`, flip → `'0'`, `sb = "10"`
   - `i = 2`: `nums[2].charAt(2) = '1'`, flip → `'0'`, `sb = "100"`
4. **Return "100"**

#### **Output:** `"100"`

---

### **Complexity Analysis**
- **Time Complexity:** \(O(n)\), since we iterate over the input array once.
- **Space Complexity:** \(O(n)\), for storing the new binary string.
