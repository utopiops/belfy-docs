---
sidebar_position: 2
---

# Page Overrides

Page overrides in Belfy allow you to customize the behavior and appearance of CRUD operations for specific entities. By defining page overrides, you can tailor the user experience to meet the specific requirements of your application.

## Defining Page Overrides

Page overrides are defined using YAML files in Belfy. To define page overrides, create a file named `page_overrides.yaml` in your project configuration folder. Each page override definition includes the following:

- **Entity Name**: The name of the entity for which the override is applied.
- **Configuration**: Configuration options for different CRUD operations, including which fields to display, whether to allow creation, reading, updating, and deletion, and any other customization options.

### Configuration Options

The configuration options for each entity include:

- **show_fields**: An array of field names to display in the list or show views for the entity.
- **allow_create**: A boolean value indicating whether to allow the creation of new entities.
- **allow_read**: A boolean value indicating whether to allow the reading of existing entities.
- **allow_update**: A boolean value indicating whether to allow the updating of existing entities.
- **allow_delete**: A boolean value indicating whether to allow the deletion of existing entities.

### Example

Here is an example of defining page overrides in the `page_overrides.yaml` file:

```yaml page_overrides.yaml
User:
  show_fields:
    - id
    - username
    - email
  allow_create: true
  allow_read: true
  allow_update: true
  allow_delete: true

Product:
  show_fields:
    - id
    - name
    - price
  allow_create: true
  allow_read: true
  allow_update: true
  allow_delete: true

Order:
  show_fields:
    - id
    - customer
    - product
    - quantity
  allow_create: true
  allow_read: true
  allow_update: true
  allow_delete: true
