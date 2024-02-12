# I_Deserializer Interface

## Definition

|             |                       |
| ----------- | --------------------- |
| Namespace   | mobject-serialization |
| Library     | mobject-serialization |
| Inheritance | I_Disposable          |

## Remarks

The `I_Deserializer` interface extends `I_Disposable` to provide methods for deserialization. It includes functionality to deserialize arrays, elements by index, and various data types from a serialized format.

## Methods

### GetArray() : I_Deserializer

Returns a deserializer for an array.

### GetElementByIndex(Index: UDINT) : I_Deserializer

Returns a deserializer for an array element using its index.

#### Parameters

| Parameters | Datatype | Description               |
| ---------- | -------- | ------------------------- |
| Index      | UDINT    | The index of the element. |

### GetKey(Key: T_MAXSTRING) : I_Deserializer

Returns a deserializer for a key.

#### Parameters

| Parameters | Datatype    | Description           |
| ---------- | ----------- | --------------------- |
| Key        | T_MAXSTRING | The key of the value. |

### GetKeyArray(Key: T_MAXSTRING) : I_Deserializer

Returns a deserializer for an array located by its key.

#### Parameters

| Parameters | Datatype    | Description           |
| ---------- | ----------- | --------------------- |
| Key        | T_MAXSTRING | The key of the array. |

### TryGetKeyObject(Key: T_MAXSTRING, Object: I_Deserializable) : BOOL

Attempts to deserialize a key to an object.

#### Parameters

| Parameters | Datatype         | Description                           |
| ---------- | ---------------- | ------------------------------------- |
| Key        | T_MAXSTRING      | The key of the object to deserialize. |
| Object     | I_Deserializable | The object to deserialize to.         |

### TryGetObject(Object: I_Deserializable) : BOOL

Attempts to deserialize data to an object.

#### Parameters

| Parameters | Datatype         | Description                   |
| ---------- | ---------------- | ----------------------------- |
| Object     | I_Deserializable | The object to deserialize to. |

### TryGetBase64(pBytes: POINTER TO BYTE, nBytes: DINT) : BOOL

Attempts to deserialize a Base64 encoded string into bytes.

#### Parameters

| Parameters | Datatype        | Description                         |
| ---------- | --------------- | ----------------------------------- |
| pBytes     | POINTER TO BYTE | Pointer to the byte array to fill.  |
| nBytes     | DINT            | The number of bytes to deserialize. |

### TryGetBool(Destination: REFERENCE TO BOOL) : BOOL

Attempts to deserialize a boolean value.

#### Parameters

| Parameters  | Datatype          | Description                       |
| ----------- | ----------------- | --------------------------------- |
| Destination | REFERENCE TO BOOL | The reference to store the value. |

... (Similar structure for other TryGet and TryGetKey methods, each tailored to their specific data type and parameters.)
