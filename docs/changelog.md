# Changelog

## v0.2.0-alpha

- Added I_Deserializer and I_Deserializable
- DeserializerGarbageCollector class. Common component used when writing your own deserializers for managing the life cycle of child nodes.
- Added dependency on mobject-collections 1.0.0.

!> This update contains the following breaking changes.

- Added AddObject and AddKeyObject to I_Seralizer, classes already created as I_Seralizer will need to implement two new methods. This is simple to add as you will only need to pass the same class back to the object. See mobject-json seralizer for an example.

## v0.1.0-alpha

- Initial
