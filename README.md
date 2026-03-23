Java Naming & Language Pattern Reference (Informal)
This document summarizes informal naming patterns commonly used in Java development. These are not official JLS (Java Language Specification) terms, but widely used in the Java community, documentation, and technical discussions.

✅ Variable Initialization Patterns

1. Blank Final: 
A final field that is not initialized at declaration but must be assigned inside every constructor.
2. Definitely Assigned: 
A variable that the compiler can prove is always initialized before use.
3. Effectively Final (JDK 8+): 
A local variable whose value is never changed, even if not marked final.
4. Constant Variable: 
A static final field initialized at declaration, typically holding immutable constants.

✅ Field Initialization Patterns

5. Lazy Initialization: 
A field initialized only when first accessed, optimizing performance or memory.
6. Double-Checked Locking: 
A thread-safe lazy initialization with minimal synchronization overhead.
7. Holder Pattern: 
A nested static class used to implement a lazy-loaded singleton safely and efficiently.
8. Phantom Reference: 
The weakest Java reference type, used for post-garbage-collection cleanup via Reference Queues.

✅ Method & Class Patterns

9. Marker Interface: 
An interface with no methods, used to signal metadata (e.g., Serializable, Cloneable).
10. Functional Interface (JDK 8+): 
An interface with exactly one abstract method (e.g., Runnable, Callable, custom lambdas).
11. Sealed Hierarchy (JDK 17+): 
Restricts which subclasses can extend a class or interface.
12. Record Pattern (JDK 16+): 
A concise syntax for immutable data carrier classes.
13. Pattern Variable (JDK 16+): 
A variable introduced through pattern matching (e.g., instanceof).
14. Unnamed Variable (JDK 21+): 
Using _ for unused variables (compiler ignores them).
15. Unnamed Pattern (JDK 22+): 
Pattern matching using _ to ignore values.

✅ Type System Patterns

16. Raw Type: 
A generic class used without specifying type parameters.
17. Reifiable Type: 
A type whose full information is preserved at runtime (e.g., List<?>, arrays).
18. Erasure: 
The compile‑time removal of generic type parameters, leaving runtime raw types.
19. Wildcard Capture: 
The compiler inferring a type variable when converting a wildcard type to a concrete one.

✅ Modern Java Patterns (JDK 21–25)

20. Unnamed Class (JDK 21 Preview): 
Allowing simplified Java programs without declaring a class explicitly.
21. String Template (JDK 21 Preview): 
A new templating syntax for expressions embedded inside strings.
22. Primitive Pattern (JDK 23 Preview): 
Pattern matching extended to primitive types.
23. Module Pattern (JDK 9+): 
Naming conventions around the Java Platform Module System (JPMS).
24. Flexible Constructor Bodies (JDK 22 Preview): 
Allowing statements before calling super() or this().
25. Derived Record Creation (JDK 23 Preview): 
Creating new record instances using with for modified copies.
