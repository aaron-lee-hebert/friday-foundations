**Friday Foundations (Week 2)**

This week I spent some time on styles of unit tests.

🧠 One idea that stuck with me:

There are 3 styles of unit tests: output-based (check a return value), state-based (check a system's condition after an operation), and communication-based (verify interactions with collaborators via mocks).

🔄 It challenged a previous assumption I had:

I'm used to reaching for mocks freely. If a class has dependencies, I would mock those to get the test in place, and up until now that has felt thorough and complete.

👀 What I'm starting to see instead:

Mocking everything couples tests to _how_ code works, not _what_ it does.

Output-based tests are the highest quality. They're small, readable, and resistant to refactoring. State-based tests are solid, but prone to over use. Usage here requires discipline. Communication-based tests should be reserved for interactions that cross an application boundary with a visible side effect.

Everything else is noise.

⚙️ Why this matters:

The style that is chosen determines long-term maintenance cost. A codebase full of mock-heavy tests can feel well-covered, but refactoring will become a maintenance burden.

👨‍💻 How I'm applying it:

I've been using Claude Code to fix bugs using strict TDD. I've been prompt-engineering it to diagnose, write a failing test, implement the minimal fix, iterate until green, then run the full suite. I've noticed that when code is written as output-based tests, the agent's loop is tight and confident. When it's leaning on mocks, things get messier and drift. The same tradeoffs apply whether a human or an AI is writing the tests.

🧐 Still working through:

When should you accept a state-based or communication-based test, instead of treating the need for one as a signal to restructure the code first?
