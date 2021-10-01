# Javascript Metaprogramming

- Writing additional code about our code.

### Code Generation

- Code writing code.

- eval
- Function Constructor
  - Last parameter is body of a function
  - All previous paramaters are arguments.

### Legacy Reflection/Introspection

- Detecting properties

  - 'in' operator lets you see if a property is in an object
    - e.g. object = { firstname: 'brian' }; 'firstname' in object;
  - Will traverse entire prototype chain, not just current object.

- Delete properties will always return true, whether the property even existed in the first place or not.

- typeof has edge cases that makes it unreliable.

### Revisied Reflection/Introspection

- Object.keys, Object.getOwnPropertyNames: keys will only get enumerable properties, so if you have properties you do not want serialized, you can set it as unenumerable.

### Object.defineProperty

- Can assign properties with extra options, such as making it non-enumerable.
- Can use Object.getOwnPropertyDescriptor() will allow looking into all properties to find option data such as configurable, enumerable...

### Object.fromEntries

- Use an array to turn into an object.

## Object.assign

- Allows cloning objects, but is actually about merging.
- You can add any number of objects and merge them together into one monolith object.

## Reflect properties

- Tends to own be on the single object, not any parents.

## Reflect.defineProperty

## Refelct.deleteProperty

- Actually returns whether it deleted something or not.

## Reflect.ownKeys

# Symbols - What are they? <-- Research this

- Collision-free Extension points.
- Can create with or without a label

# Intercession

- Intercepting behavior
- Proxy <-- Another version like Reflect, needs research.
