---
sidebar_position: 3
---

# Navbar

The navbar in Belfy provides navigation links to different sections or pages of your application. You can customize the navbar to include links to various entities, dashboards, or other relevant sections of your application.

## Navbar Configuration

Navbar configuration in Belfy is defined using a YAML file named `navbar.yaml`. This file contains a list of items representing the navigation links in the navbar.

### Configuration Options

Each item in the navbar configuration represents a navigation link and can be a string indicating the label of the link.

### Example

Here is an example of defining navbar items in the `navbar.yaml` file:

```yaml navbar.yaml
items:
  - Product
  - Order
  - Category
```