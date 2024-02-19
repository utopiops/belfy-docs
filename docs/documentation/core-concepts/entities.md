---
sidebar_position: 1
---

# Entities

Entities are the fundamental building blocks of your CRUD applications in Belfy. 
They represent the different types of data that your application will manage. Each entity consists of properties that define the structure of the data.

## Defining Entities

Entities are defined using YAML files in Belfy. You **must** have a file named `entities.yaml` to define your entities. Each entity definition includes the following:

- **Name**: The name of the entity, which serves as its identifier.
- **Properties**: An array of properties that define the structure of the entity. Each property includes a name and a type, and can optionally specify additional attributes such as whether it is a primary key or a reference to another entity.

### Property Structure

Each property in an entity definition has the following structure:

- **Name**: The name of the property.
- **Type**: The data type of the property, which can be one of the following: `string`, `number`, `boolean`, `datetime`, or `text`. File and image types are not currently supported, but will be added in the near future.
- **Optional Attributes**:
  - **primaryKey**: Indicates whether the property is a primary key.
  - **reference**: Specifies the name of the entity that this property references, if applicable.

:::tip
In addition to the properties defined in the YAML file, generators may add a field named "id" by default, which serves as the primary key for the entity. However, specific instructions about the primary key and the "id" field can be found in the documentation of the respective generators.
:::

### Example

Here is an example of defining two entities in the `entities.yaml` file:

```yaml title=entities.yaml
- name: User
  properties:
    - name: id
      type: string
      primaryKey: true
    - name: username
      type: string
    - name: email
      type: string

- name: Product
  properties:
    - name: id
      type: string
      primaryKey: true
    - name: name
      type: string
    - name: price
      type: number

- name: Order
  properties:
    - name: id
      type: string
      primaryKey: true
    - name: customer
      type: string
      reference:
        model: User
        property: id
    - name: product
      type: string
      reference:
        model: Product
        property: id
    - name: quantity
      type: number