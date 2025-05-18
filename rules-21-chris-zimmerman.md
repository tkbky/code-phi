## **The 21 Rules of Programming: How to Write Better Code by Chris Zimmerman**

These rules are from the book The Rules of Programming: How to Write Better Code by Chris Zimmerman. Zimmerman is a co-founder of Sucker Punch Productions, known for games like Sly Cooper, inFamous, and Ghost of Tsushima. In this book, he draws from decades of experience in professional software development, especially in game development, to lay out 21 practical, opinionated rules for writing clean, effective code.

The rules are not academic theories — they're lessons learned through real-world coding, code reviews, and debugging. They emphasize clarity, simplicity, practicality, and professionalism — aiming to help developers build maintainable, robust systems while avoiding common pitfalls like overengineering, premature optimization, and clever-but-unreadable code.

### 1. **As Simple as Possible, But No Simpler**

Strive for simplicity. Avoid unnecessary complexity, but don’t oversimplify to the point that it breaks functionality. Implement only what's needed—no more, no less.

### 2. **Let Your Code Tell Its Own Story**

Write code that is self-explanatory. Use meaningful names and a clear structure so others (and your future self) can understand your intent without extra documentation.

### 3. **Localize Complexity**

Keep complex logic contained. Isolate it within modules or functions to prevent it from spreading throughout the system, making everything harder to manage.

### 4. **Generalization Takes Three Examples**

Don't abstract or generalize too early. Wait until a pattern appears in at least three places before turning it into a reusable component. This helps avoid needless abstraction.

### 5. **Work Backward from Your Result**

Start by clearly defining the end goal. Let the outcome guide your implementation, rather than coding aimlessly and hoping it leads somewhere useful.

### 6. **The First Lesson of Optimization Is: Don’t**

Don’t optimize prematurely. Focus on getting your code working and readable first. Optimize only when there's a real need, and you understand the bottleneck.

### 7. **A Good Name Is the Best Documentation**

Use names that describe what the code does or represents. A well-named variable, function, or class can eliminate the need for a comment altogether.

### 8. **Bugs Are Contagious**

One bug often leads to more. Fix issues as soon as they arise to prevent them from spreading and creating deeper problems down the line.

### 9. **Eliminate Failure Cases**

Design your system to gracefully handle errors. Check inputs, validate assumptions, and make failure modes clear and recoverable wherever possible.

### 10. **Code That Isn't Running Doesn't Work**

Dead or unused code is a liability. It can rot, confuse, and break things unexpectedly. Regularly clean up or update code that is no longer used.

### 11. **Sometimes You Just Need to Hammer the Nails**

Not everything needs to be clever or beautiful. When you're stuck, a straightforward, practical solution is often the best path forward.

### 12. **Code Reviews Are Good for Three Reasons**

They catch bugs, spread knowledge across the team, and uphold coding standards. Make code reviews a routine and collaborative part of development.

### 13. **Code Comes in Four Flavors**

Recognize the type of code you're writing—whether it's infrastructure, glue, algorithmic, or business logic—and adapt your approach to suit the context.

### 14. **Pull the Weeds**

Like a garden, your codebase needs constant maintenance. Refactor, simplify, and clean up regularly to prevent the accumulation of technical debt.

### 15. **If Something Doesn’t Work, It’s Your Fault**

Take ownership. If the code fails, assume responsibility—even if the problem originated elsewhere. That mindset leads to faster fixes and better quality.

### 16. **Some Tools Should Be Left in the Toolbox**

Just because a tool or technology exists doesn’t mean you should use it. Make sure it's the right fit before adding complexity to your stack.

### 17. **Big Projects Need Simple Designs**

Complexity scales poorly. The larger the system, the more important it is to keep the architecture simple and understandable.

### 18. **Not Every Problem Has an Elegant Solution**

Sometimes the best fix is messy. Don’t delay progress chasing perfection when a working, practical solution is within reach.

### 19. **The Best Code Is No Code at All**

The fewer lines you write, the fewer bugs you introduce. If you can solve a problem without writing new code, that’s often the better option.

### 20. **Don’t Be Clever**

Clever code might feel good to write, but it’s often hard to read, debug, and maintain. Prioritize clarity and simplicity over ingenuity.

### 21. **The Only Thing Worse Than a Comment Is No Comment**

Write comments sparingly, but make them count. Explain _why_ something is done, especially when the logic is non-obvious. Avoid obvious or redundant comments.
