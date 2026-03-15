

### Question 1 — Java / Spring

In a Spring Boot application, can you explain the difference between `@Component`, `@Service`, `@Repository`, and `@Controller`? Beyond the naming convention, are there any practical differences in how Spring treats them?

---

These annotations are used for marking services in spring boot application that are later going to be used for dependency injection during startup of application.

- `@Component` is the broadest annotation. We can use it mark any class that will be injected, e.g. configuration class
- `@Service` is used to mark services,
- `@Repository` is used to mark repository level classes
- `@Controller` is used to mark controllers

All of these annotation do not differ under the hood. Their usage comes down to Spring convention, but they all work the same way

---

**Feedback**

These annotations are used for marking services in spring boot application that are later going to be used for dependency injection during startup of application.

- `@Component` is the broadest annotation. We can use it mark any class that will be injected, e.g. configuration class
- `@Service` is used to mark services,
- `@Repository` is used to mark repository level classes
- `@Controller` is used to mark controllers

All of these annotation do not differ under the hood. Their usage comes down to Spring convention, but they all work the same way


### Question 2 — Frontend / Angular

Since you've got strong Angular experience: Can you explain what **change detection** is in Angular, and what's the difference between the `Default` and `OnPush` change detection strategies? When would you choose `OnPush` and what do you need to be careful about when using it?

--- 

No idea


### Question 3 — Java / Spring

What is the difference between `HashMap` and `ConcurrentHashMap` in Java? In what scenario would you choose one over the other, and what would happen if you used a regular `HashMap` in a multi-threaded environment?

---

`ConcurrentHashMap` is a version of regular `HashMap` made for multi threaded environment. If we were to use `HashMap` in multi threaded environment we would risk encountering race condition when two different processes would want to operate on the same data stored in `HashMap`.

---
**Feedback:**

Good — you identified the core purpose and the race condition risk. That's the right instinct. But for a strong mid-level interview, they'd expect you to go a bit deeper. A couple of things that would strengthen your answer:

**How does `ConcurrentHashMap` achieve thread safety?** It uses **segment-level (bucket-level) locking** rather than locking the entire map. This means multiple threads can read and write to different segments concurrently, which makes it much more performant than wrapping a `HashMap` with `Collections.synchronizedMap()` — which locks the entire map for every operation.

**What actually goes wrong with `HashMap` in multi-threaded context?** Beyond just race conditions on data, in older Java versions (pre-8), concurrent puts could cause an **infinite loop** during rehashing because of how linked list entries were reordered. In modern Java it won't loop, but you can still get **lost updates, corrupted state, or unexpected `NullPointerException`s**.

**Bonus point interviewers love:** `ConcurrentHashMap` does not allow `null` keys or values, while `HashMap` allows one `null` key and multiple `null` values. This sometimes catches people off guard.

**Score: 6/10** — Correct direction but too surface-level. Practice adding one layer of depth to your answers — the "how" behind the "what."

### Question 4 — Behavioral

Tell me about a time when you had to deal with a significant technical disagreement with a colleague. How did you handle it and what was the outcome?

---

