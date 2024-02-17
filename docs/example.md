---
sidebar_position: 2
---

# Example

1. Place the following files in an arbitrary folder `<path/to/folder>`:


```yaml title="entities.yaml"
- name: User
  properties:
    - name: name
      type: string

- name: Product
  properties:
    - name: name
      type: string
    - name: price
      type: number
    - name: description
      type: text

- name: Order
  properties:
    - name: customerId
      type: number
      reference: 
        model: User
        property: id
    - name: totalAmount
      type: number
    - name: status
      type: string

- name: Category
  properties:
    - name: name
      type: string
    - name: description
      type: text
```

```yaml title="navbar.yaml"
items:
  - Product
  - Order
  - Category
```

```yaml title="page_overrides.yaml"
Product:
  show_fields:
    - name
    - price
    - description
  allow_create: true
  allow_read: true
  allow_update: true
  allow_delete: true

Order:
  show_fields:
    - customerId
    - totalAmount
    - status
  allow_create: true
  allow_read: true
  allow_update: true
  allow_delete: true

Category:
  show_fields:
    - name
    - description
  allow_create: true
  allow_read: true
  allow_update: true
  allow_delete: true
```

2. Run this command in the terminal

```bash
npx belfy create
```

3. Answer the questions based on your preferences

![example](/img/example-base-questions.png)

4. Choose `fs-express-handlebars` as the full-stack option

![fs option](/img/example-fs-options.png)