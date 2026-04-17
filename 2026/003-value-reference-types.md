# Friday Foundations (Week 4)

This week I spent some time on a foundational topic that every .NET developer thinks they understand, until they try to explain it. Value types vs. Reference types.

🧠 One idea that stuck with me:

If you hand someone a photo of your home (value type), they can look at it. If they write on it, your original is fine. When you hand someone your address (reference type), you're both talking about the same home. If they decide to repaint the door, you might come home to a red door.

That's the difference between these two concepts in code. Some data gets copied when it's passed around, while other data gets shared. Code behaves very differently depending on which one you're dealing with.

🔄 It challenged a previous assumption I had:

Depending on how a method was defined, passing data into a method always gave that method its own isolated copy to work with. Similar to handing over the photo. It's safe, contained, and there's no surprises. This is only sometimes true.

👀 What I'm starting to see instead:

For many common data types in .NET (objects, lists, custom classes) you're handing over the address, not a photo. The method is looking at the same house you are. Any changes it makes, you'll see when you get back. Knowing which one you're dealing with turns vague bugs into obvious ones.

⚙️ Why this matters:

Some of the hardest bugs to track down aren't logic errors, they can be surprise sharing. Two parts of a system quietly modifying the same piece of data, each assuming they had their own copy. This shows up in APIs, services, and data layers. It's never really dramatic, but it's responsible for wrong results that are hard to reproduce.

👨‍💻 How I'm applying it:

I'm asking a new question when I write or review code: should this method be able to affect the data the caller passed in, or should it be working on its own copy? Sometimes sharing is exactly what you want; however, it needs to be a choice, not an accident.

🧐 Still working through:

The rules about where data physically lives in memory (the stack vs. the heap) have more nuance than the simple version I learned. The type alone doesn't tell the whole story, but context matters too.
