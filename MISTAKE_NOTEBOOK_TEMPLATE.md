# 📓 GATE CS 2027 — MISTAKE NOTEBOOK & PYQ ERROR LOG
**The Single Most Powerful Weapon for a Top 100 AIR**

> *"Success in GATE does not come from solving 10,000 new questions; it comes from never repeating a mistake you have made once."*

---

## 🎯 The 4 Error Categories (Tag Every Mistake)

Whenever you get a PYQ or Mock Test question wrong, categorize it immediately:

1. **`[TYPE-A: CONCEPT GAP]`**  
   *Definition*: You did not know the underlying theorem, property, or standard technique.  
   *Action*: Re-watch the specific 15-minute lecture segment, re-read standard book definition, write the complete concept into notes.

2. **`[TYPE-B: QUESTION MISINTERPRETATION / TRAP]`**  
   *Definition*: You misread words like "MUST BE TRUE" vs "CAN BE TRUE", "INCORRECT", "AT LEAST", missed boundary conditions ($n \ge 1$), or fell into a distractor trap.  
   *Action*: Write down the exact trap phrase in bold red ink or bold markdown.

3. **`[TYPE-C: CALCULATION / VIRTUAL CALCULATOR / NAT SLIP]`**  
   *Definition*: Made an arithmetic error, wrong unit conversion (Bytes vs Bits, ms vs $\mu s$, decimal vs binary rounding), or typed incorrectly on the virtual keypad.  
   *Action*: Re-do the exact calculation 3 times cleanly on rough paper.

4. **`[TYPE-D: FORMULA / ALGORITHM AMNESIA]`**  
   *Definition*: Forgot the exact formula (e.g., Belady's anomaly bounds, IEEE 754 exponent bias, Dijkstra time with binary heap vs Fibonacci heap).  
   *Action*: Add to the 1-Page Formula Summary Sheet immediately.

---

## 📋 Mistake Entry Format

Use the following Markdown template to log every erroneous or guessed question:

```markdown
### 🔴 Mistake Entry #[001]
- **Date**: 2026-09-25
- **Subject**: Discrete Mathematics
- **Topic**: Mathematical Logic (Predicate Logic & Quantifiers)
- **Source**: GATE 2015 Set-1 (Q.24) / GATE Overflow URL: [Link]
- **Error Type**: `[TYPE-B: QUESTION MISINTERPRETATION]`

#### 1. What was the Question?
*Brief summary or copy of statement:*
"Which of the following first-order logic formulas is equivalent to $\forall x (P(x) \rightarrow Q(x))$?"

#### 2. What Mistake Did I Make?
I incorrectly assumed $\forall x (P(x) \rightarrow Q(x))$ distributes as $(\forall x P(x)) \rightarrow (\forall x Q(x))$. 

#### 3. Why is that Wrong? (The Core Truth)
Universal quantifier $\forall$ distributes over $\land$, but NOT over $\rightarrow$ or $\lor$.  
Counter-model: Let domain be integers, $P(x)$ = "x is even", $Q(x)$ = "x is divisible by 4".  
True equivalent form: $\neg \exists x (P(x) \land \neg Q(x))$ or $\forall x (\neg P(x) \lor Q(x))$.

#### 4. The Golden Rule / Anti-Trap Takeaway:
> ⚠️ **RULE**: $\forall x (A \rightarrow B) \not\equiv (\forall x A) \rightarrow (\forall x B)$.  
> Always convert implications to $\neg A \lor B$ before attempting quantifier scope changes!

#### 5. Re-attempt Status:
- [ ] Round 1 (After 3 Days): PASSED / FAILED
- [ ] Round 2 (After 14 Days during Subject Revision): PASSED / FAILED
- [ ] Final Sprint Pass (January 2027): PASSED
```

---

## 🔄 The 3-Tier PYQ Re-attempt Protocol

1. **Tagging while Solving**:
   - `🟢 Green (Level 1)`: Solved on first attempt within 2.5 minutes without checking solution $\rightarrow$ No revisit needed.
   - `🟡 Yellow (Level 2)`: Solved correctly but took $> 4$ minutes or had slight confusion $\rightarrow$ Revisit in Revision Phase 1.
   - `🔴 Red (Level 3)`: Got wrong, guessed, or needed to peek at the answer key $\rightarrow$ Enter into Mistake Notebook + Re-solve independently in 72 hours.

2. **Re-attempt Cycles**:
   - **Day +3**: Re-solve the Red questions without looking at the notebook.
   - **Day +14**: Re-solve Yellow + Red questions during weekend revision.
   - **January Sprint**: Re-solve ALL Red questions from the entire 35-year archive.
