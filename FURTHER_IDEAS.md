## Backing up code

Users won't have git on their smartphones. To support this, we need to
provide a remote service for them to back up.

## Exchanging code

Users want to be able to send programs to other users. Sharing
snippets, games, RPC or elaborate interactions.

To support this, we need a capability system. Much like Android
provides app permissions, but JIT rather than up-front. E and Pony
both provide this.

## Killer app

Most programming tools on smartphones are gimmicks. We need users to
be able to show useful/interesting/fun things they have made.

The test of this project's success is what users build, not how
brilliant the IDE is.

Furthermore, building on top of messaging could be a bootstrap. Users
open their messaging apps regularly, so they have more opportunities
to be in the app and reflecting on what they'd like to tinker with.

## Introspection

Code should be cross-referencable, and include sources. The entire
system should be mutable, but with save points (like Smalltalk, or
Emacs).

## Touch-driven IDE

We must minimise keystrokes: typing is awkward on a touchscreen.

Allowing users to work on the AST as far as possible (see the Lisping
demo, or lispy.el) would go a long way.

If we provide a structured editor on an AST, we don't necessarily need
a syntactically unambiguous display. Semicolons, for example, would be
unnecessary.

Instead, a contextual halo (again see the Lisping demo, or halos in
Smalltalk) must be as powerful as possible. This might include:

1. Dragging code in/out of control structures (cf paredit
   barf/slurp). For example, dragging a statement into an if block or
   loop body.

2. Touch-renaming for variables (never allow a variable to edited in
   isolation).
   
3. Snippets. Types may provide their own snippets (e.g. a list
   provides an iteration loop snippet) to minimise
   typing. Placeholders should be filled in with fresh, valid variable
   names.
   
4. Hole-based refinement. If we have static typing, this saves many
   keystrokes.
   
5. Unqualified imports. I imagine we will want `import foo from lib;
   foo` rather than `import lib; lib.foo` as qualified variables are
   extra typing.
   
Open questions:

1. How do we handle expanding selection? If I touch `foo` in `if foo
   bar() barz()`, do I select just the loop condition, or the whole
   block? How do I change selection range?
   
2. What about extracting functions? (related to expanding selection)

3. How is code organised? Do we have files or a Smalltalk-like
   browser? 
   
4. What about when we actually need prose? For example, docstrings and
   usage examples. I suspect smartphone users dislike typing.
   
5. How do we provide a website promoting the app and its content,
   without caving to the temptation to scale up the IDE for other
   platforms? If there's an escape hatch, the smartphone IDE will not
   get the necessary focus.
   
6. What do users want to build? What is the hello world for our app?
   Suggestion: triggering a notification.

7. How do we onboard users? What should they see first?
