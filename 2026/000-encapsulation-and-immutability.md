I'm trying to build a new habit. I've put personal learning on the backburner, and I want to plug up holes I've discovered in my own software development journey these past 7+ years. Hopefully this provides value for you, too!

**Friday Foundations (Week 1)**

This week I spent some time revisiting the difference between _encapsulation_ and _immutability_.

🧠 One idea that stuck with me:

**Encapsulation** means hiding implementation details, so that callers cannot access an object's internals directly, whereas **immutability** is concerned with the state of an object not being able to change. If a "different" version of an object is needed, then a new value gets created instead of modifying an existing one.

⚙️ Why this matters:

If an application is following a functional style or architecture, unit testing becomes trivial. A test that is stateful must understand mocked dependencies, build & configure state, and arrange state before acting and asserting results.
When possible, using pure functions with functional tests eliminates those state dependencies, leaving you to test just a _behavior_.

This points back to what makes a good unit test:

1. Protection against regressions
2. Resistance to refactoring
3. Fast feedback
4. Maintainability

👨‍💻 How I’m applying it:

Instead of trying to apply unit tests at the end of a work item, I'm first going to look at a system and determine what's expected to change. Then, I should be able to produce unit tests that protect the current behavior (if they didn't exist) and introduce additional tests for the behavior coming into the system.

🧐 Still working through:

A unit test falls into three different styles: "output-based", "state-based" and "communication-based". Functional concepts apply to "output-based" tests, but an understanding of "state-based" and "communication-based" tests are important, too. Something to follow up and cover next week. 💪
