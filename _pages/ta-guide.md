---
layout: single
title: "TA Guide: Automata & Formal Languages"
permalink: /teaching/ta-guide/
author_profile: true
description: "A practical guide for new teaching assistants (TAs) in Automata & Formal Languages: grading workflows, office hours strategies, and academic integrity policies."
---

This is a pratical guide for new teaching assistants (TAs) in the course *Automata & Formal Languages*. It covers grading workflows, office hours strategies, and academic integrity policies. It is based on my experience as a Graduate Teaching Assistant at the [University of Minnesota Duluth](/teaching/). The goal is to maintain high academic standards, ensure student comprehension, and maintain integrity and transparency during the course. I am also very inspired by [Mário S. Alvim's Teaching Principles](https://msalvimjr.github.io/webpage-dcc/faqs/teaching-grading/).

---

## I. The Grading & Feedback Lifecycle

In a course that builds sequentially, timely feedback is essential for student progress. Grades should, ideally, be returned **within one week** of submission, but it is acceptable to extend this to **two weeks** in unforeseen circumstances. The absolute deadline for returning grades is **before the lecture preceding the next exam** so that students can use the feedback to prepare for the next assessment.

You have the discretion to allow a resubmission or a "fix-it" for credit. **Only** grant this to students who:

1. Demonstrated a genuine, high-effort attempt on the original submission.
2. Are frequent attendees of office hours.

Before the start of the semester, confirm with the instructor whether you are allowed to offer resubmissions for credit. There might be a penalty for late submissions or resubmissions that you might need to enforce. If you are unsure, consult the instructor before making a decision.

---

## II. Office Hours: Managing Student Needs

Students will inevitably have difficulty understanding the course content or finding the right path to solve a problem. Your role as a TA is to point the student in the right direction and help them grasp the underlying logic without removing the intrinsic difficulty of the course (refer to Principle #1 of [Mário S. Alvim's Teaching Principles](https://msalvimjr.github.io/webpage-dcc/faqs/teaching-grading/)). Adapt your approach based on the level of preparation the student demonstrates when they arrive:

### 1. The "Stuck" Student (High Effort)

These students come prepared with pages of scratch work and can point to the specific step where their logic broke down. Because they have already put in significant effort, your goal is to help them bridge the precise point of confusion. Identify the specific step they misunderstood, point them directly to the relevant formal definition in the textbook (for example, reminding them how the transition function $\delta$ is defined for an NFA versus a DFA), and re-explain that specific logic.

### 2. The "Lost" Student (Medium Effort)

These students regularly attend lectures but struggle to translate and interpret theoretical concepts into concrete solutions. Instead of handing them the answer, ask targeted questions about the core concepts to locate their knowledge gaps. Break the homework problem down into smaller, isolated sub-problems and guide them to complete one step at a time in front of you. These are my favorite students, because you can see how far the progressed at the end of the semester. It was very rewarding for me to see their improvement.

The example I remember the most is a student that was not able to understand the conversion of a CFG to a CNF. We went through the example on Sisper's book and related each step with the formal definition of CNF. They need to understand why we are doing each step. Another very common example is when they do not understand the pumping lemma for both regular and context-free languages and how to apply them. Since they need to understand the "why" behind the lemma, I usually explain the proof and how the Demon's Game is essentially a proof by contradiction.

### 3. The "Shortcut" Student (Zero Effort)

These students have not read the assigned material and are looking for easy instructions or direct answers so they can finish the assignment quickly. Maintain a firm **no shortcuts** policy. If a student has not read the relevant chapter, ask them to sit down in office hours and read the specific section right there. Let them know: *"Start reading here; I'll check back in 10 minutes to see if you have a specific question about the logic."* Only offer assistance once they demonstrate they have engaged with the material.

---

## III. Grading Philosophy, Workflow & Records Securement

Grading is an assessment of **comprehension**, not just a clerical check for a "right" final string. Every evaluation should reflect whether the student actually understands what they are doing.

### 1. Partial Credit vs. Binary Grading

Partial credit is encouraged when a student clearly understands the topic but makes a minor error—the "silly mistake" rule. However, if it is clear that the student does not understand the underlying theory, do not award pity points; **award a 0**. Furthermore, for questions that are labor-intensive to decode but have very specific, compact answers (such as writing a regular expression for a given language), evaluate them on a **binary (Correct/Incorrect)** basis. Do not waste time trying to decipher non-functional, convoluted strings to award partial credit.

### 2. Integrity Check

Every student must be able to explain their submitted answers in person. If a submission contains nonsensical logic or looks copied yet somehow arrives at the correct answer, **award a 0**. When doing so, leave a clear comment on Canvas: *"Please see me during office hours to explain your logic for this question to receive credit."* If they can explain their reasoning during office hours, you may restore the grade; if they cannot, the zero stands.

You can be surprised with evidence of unoriginal work. You need to respond according to its source:

* **Internet & External Sources:** Students must explicitly cite any external source used to solve a problem. If you discover an unreferenced solution copied from an external source, assign a grade of 0 and request an in-person explanation during office hours.
* **Peer-to-Peer Copying:** If you notice identical idiosyncrasies—such as identical non-standard layouts or unique, highly specific errors—shared between two or more students, **report it to the instructor immediately**. Do not attempt to resolve peer-to-peer copying cases on your own and forget about it. The instructor and the department head will handle the situation. If the student try to reach you to discuss the situation, politely redirect them to the instructor.

### 3. Canvas Security & Submission Verification

Maintaining an unalterable digital paper trail is necessary to protect both you and the students. Every student **must** submit their homework through Canvas, as it stores the exact version used for grading. This protects you if a student claims their work was tampered with and prevents students from altering grading notes or marks after evaluation. If you prefer to grade physical paper copies, the student must still upload their assignment to Canvas **and** hand in the physical paper copy. Never grade a submission that lacks a digital record on Canvas.

### 4. The TA's Pre-Grading & Post-Grading Workflow

Before grading a single assignment, solve the homework yourself (or take a submission from a top student, verify its accuracy, and use it as your key). Next, perform a quick scan by flipping through roughly 10 random submissions to gauge common pitfalls and understand the range of student responses. Use this scan to finalize your rubric and configure it directly within Canvas before entering any marks. Finally, publish the official solutions on Canvas only after the second-chance deadline has passed, but always before the lecture preceding the next exam.

Sometimes I forget to look into some submissions before I define the rubric. Many times I had to go back and regrade some submissions becuase I did not consider some edge cases. Defining a good rubric is very important when you are using partial credit.

---

### Disclaimers & Licensing

**Notice on Content Generation:** This guide was developed with the assistance of a generative AI model (Gemini). The core principles, workflows, and policies are derived from my personal experience as a Graduate Teaching Assistant at the **University of Minnesota Duluth**. I assume full responsibility for the methodology and content.

**License:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

**How to cite:**
> Oliveira, José C. *TA Guide: Automata & Formal Languages*. Available at: [https://josecoliveira.github.io/teaching/ta-guide/](https://josecoliveira.github.io/teaching/ta-guide/)
