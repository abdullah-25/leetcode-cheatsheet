# Stages of an Interview

_Report Issue_

Most algorithmic interview rounds are between **45–60 minutes**. The interviews can be broken down into stages, and at each stage, there are multiple things you should do to maximize your chances of success. Let's break it down.

---

## 1. Introductions
- Interviewer will introduce themselves and ask you to do the same.  
- **Prepare and rehearse** a 30–60 second introduction: summarize education, work experience, and interests.  
- **Tips:**
  - Smile and speak with confidence.
  - Pay attention to the interviewer’s intro — you can ask questions about it later.
  - If they mention something you share in common (work or hobby), mention it.

---

## 2. Problem Statement
- Interviewer gives you a problem statement (usually pasted into a shared editor).  
- **Steps:**
  1. Paraphrase the problem back to confirm understanding.
  2. Ask clarifying questions:
     - Input types (only integers or others?)
     - Sorted vs unsorted?
     - Guaranteed non-empty or possibly empty?
     - How to handle invalid inputs?
     - Expected input size?  
       - Small `n` → brute force/backtracking might be fine.  
       - Medium `n` (100–1000) → `O(n²)` might be optimal.  
       - Large `n` → need better than `O(n)`.
  3. Walk through provided test cases.
- Clarifying questions show attention to detail and edge-case awareness.

---

## 3. Brainstorming DS&A
- Figure out what **data structure or algorithm** is applicable.  
- Break the problem down, recognize patterns, and think about complexity.  
- **Think out loud**:
  - Shows tradeoff consideration.
  - Opens the door for interviewer hints.
- Before coding, outline the rough steps and confirm with the interviewer.
- **Be receptive**:
  - Interviewers will hint if you’re going off-track.  
  - Don’t be stubborn; explore their hints.

---

## 4. Implementation
- Once you have agreement on the approach, start coding.  
- **Tips:**
  - Confirm use of libraries/modules before importing.
  - Explain decisions as you code (e.g., “using a set to avoid cycles”).
  - Write clean, readable code (follow language conventions).
  - Avoid duplication — use arrays, loops, or helper functions.  
  - Don’t suffer silently if stuck. Communicate concerns.
  - Brute force first (if needed), then optimize with interviewer involvement.

---

## 5. Testing & Debugging
Interview environment varies:

1. **Built-in test cases (like LeetCode):**
   - Stresses your code with all edge cases.
   - Less pressure to write your own tests.

2. **Write your own tests (code can run):**
   - Shared editor with runtime support.
   - Write function calls and `print()` results.
   - Include variety: edge cases, intuitive inputs, invalid inputs.

3. **Write your own tests (no runtime):**
   - Shared editor without code execution.
   - Walk through test cases manually.
   - Track variable states and outputs as you go.

**Debugging tips:**
- Add print statements.
- Walk through with small test cases.
- Compare expected vs actual variable values.
- Stay vocal — easier for interviewer to help.

---

## 6. Explanations & Follow-ups
After coding, expect to answer questions such as:
- **Time & space complexity**:
  - Worst-case required; mention average case if notably faster.
- **Why did you choose X?**
  - Be ready to justify data structures, algorithms, loops, etc.
- **Could the algorithm be improved?**
  - Be cautious — ok to be wrong, not ok to be confidently wrong.

If time remains:
- May get a **new problem** → restart from step 2.
- Or **follow-ups** → new constraints, improved complexity, etc.

This is why you must understand solutions, not just memorize them.

---

## 7. Outro
- Interviewer will usually allow you to ask questions.  
- **Remember:** Interviews are two-way. Use this to evaluate the company.  
- Good questions to ask:
  - What does an average day look like?
  - Why did you join this company?
  - Favorite and least favorite parts of the job?
  - What kind of work will I do?
- **Pro tip:** Read the company’s tech blog beforehand and ask about it.  

**Tips:**
- Show genuine interest, smile, listen actively, and ask follow-ups.
- Avoid looking bored/uninterested — even strong technical performance can’t save a bad impression here.

---
