**Static** keyword in C++ can describe two situations:
- When a static variable is outside of a class
- When a static variable is a member of a class

## Static outside of a class
In this case, static variable makes [[linker]] to search for its definition only in this variable's translation-unit. This means that the linker will skip any variable definition outside of its translation-unit.

## Static inside of a class
When static variable is inside of a class, it is interpreted as a unique member of a class which isn't bound with any instance of a class. It's simply one unique variable that is shared. That means that it exists without any particular instance. 
It's also worth knowing, that any static variables or methods will work only with other static members, because static members don't see any non-static members which are bound to specific instances.