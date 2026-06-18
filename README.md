# Laravel Grocery List

## Opdracht 1 - Database Diagram

### Database Diagram

![Database Diagram](docs/database-diagram.png)

### DBML

```dbml
Table categories {
  id int [pk, increment]
  name varchar [not null]
  created_at timestamp
  updated_at timestamp
}

Table items {
  id int [pk, increment]
  name varchar [not null]
  description text
  category_id int [not null]
  created_at timestamp
  updated_at timestamp
}

Ref: items.category_id > categories.id
```

## Beschrijving

Dit project is ontwikkeld voor de Laravel-opdrachten. Het betreft een boodschappenlijst-applicatie met items en categorieën.

### Relatie

- Een categorie kan meerdere items bevatten.
- Een item behoort tot precies één categorie.
