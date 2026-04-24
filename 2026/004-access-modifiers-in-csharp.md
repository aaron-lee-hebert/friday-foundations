**Friday Foundations (Week 5)**

This week I revisited access modifiers in C#, or "who gets to see what" in a codebase. It's one of the quieter ways software systems either hold themselves together or slowly fall apart.

🧠 One idea that stuck with me:

In software, not every piece of code needs to be visible to every other piece. You must deliberately control what's exposed and what stays hidden. Think of it like an office building. Some rooms are open to the public, some for employees only, some for one specific department, and some are for the one team that actually maintains the building's infrastructure. The rooms don't change; however, who has a key is a deliberate decision. Most developers may just hand out "master keys" by default.

🔄 It challenged a previous assumption I had:

Previously, I've thought access modifiers in code were mostly about security, or keeping bad actors out. When something didn't feel like a security risk, I didn't think much about restricting it.
What's missed is that these controls aren't just about threats from outside, but they're about protecting the system from itself. One part of the codebase may accidentally reach into another part it was never meant to see or touch, and that's a problem!

👀 What I'm starting to see instead:

Good software architecture is about boundaries, and boundaries are only real if something enforces them. You can document the rules, you can talk about them in reviews, you can put them in a wiki, but if the compiler doesn't enforce them, they'll eventually get crossed. Deliberately restricting visibility is how you make the architecture real, not just theoretical.

⚙️ Why this matters:

When every part of a system can reach every other part, small shortcuts compound. A developer under deadline pressure takes the most direct route, even if that route skips three layers of design that existed for good reasons. Over time, the system becomes harder to change, harder to test, and harder to understand. Tightening visibility upfront is cheap, but untangling later will be expensive.

👨‍💻 How I'm applying it:

Before I make something visible to the rest of the codebase, I'm asking the following questions:

1. Does anything outside of the current assembly need to see this?

If the answer is "No", then the best route would be to use the 'internal' modifier for types and 'private' for members.

2. Does a subclass need to see this?

If the answer is "Yes", then the next path would be to use a 'protected' modifier. If subclasses are internal only, then one could use 'private protected'. If external subclasses need to see this, then 'protected internal' (same assembly OR sublcass, including external) or 'public'.

3. Does the entire application need to see this?

If the answer is "Yes", the the only option is 'public'; however, this needs to be the final question, not the first.
