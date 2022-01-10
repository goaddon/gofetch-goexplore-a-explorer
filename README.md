# gofetch-goexplore-a-explorer
This explorer enables merchants browse the data fetched by [Gofetch](https://goaddon.com/en/addons/5b9ff6463ab42f43522b30cf) on websites hosted by [Goexplore](https://goaddon.com/en/addons/5bb227d283c3360abe01e036)'s A framework.

# Index recommendations

The explorer queries your MongoDB database for data. In order to avoid unhealthy resource consumption in your database you should consider creating the following indexes through your Goaddon project account.

#### Used by categories\__index

```json
{
  "klass": "categories",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "name": 1
      }
    },
    {
      "key": {
        "company_id": 1,
        "remote_id": 1,
        "name": 1
      }
    }
  ]
}
```

#### Used by categories\__show

```json
{
  "klass": "categories",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by countries\__index, orders\__show

```json
{
  "klass": "countries",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "name": 1
      }
    }
  ]
}
```

#### Used by countries\__show

```json
{
  "klass": "countries",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by customers\__show

```json
{
  "klass": "customers",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by customers\__show

```json
{
  "klass": "orders",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "customer_id": 1,
        "initialized_at": -1
      }
    }
  ]
}
```

#### Used by delivery_methods\__index

```json
{
  "klass": "delivery_methods",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "name": 1
      }
    }
  ]
}
```

#### Used by delivery_methods\__show, orders\__show

```json
{
  "klass": "delivery_methods",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by payment_methods\__show, orders\__show

```json
{
  "klass": "payment_methods",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by statuses\__show, orders\__show

```json
{
  "klass": "statuses",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by orders\__index

```json
{
  "klass": "orders",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "initialized_at": -1
      }
    },
    {
      "key": {
        "company_id": 1,
        "order_number": 1,
        "initialized_at": -1
      }
    },
    {
      "key": {
        "company_id": 1,
        "email": 1,
        "initialized_at": -1
      }
    }
  ]
}
```

#### Used by orders\__show, variants\__show

```json
{
  "klass": "orders",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by orders\__show

```json
{
  "klass": "shipments",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "order_id": 1,
        "created_at": 1
      }
    }
  ]
}
```

#### Used by orders\__show

```json
{
  "klass": "order_lines",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "order_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by orders\__show

```json
{
  "klass": "invoices",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "order_id": 1,
        "created_at": 1
      }
    }
  ]
}
```

#### Used by orders\__show

```json
{
  "klass": "credit_notes",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "order_id": 1,
        "created_at": 1
      }
    }
  ]
}
```

#### Used by orders\__show, variants\__show

```json
{
  "klass": "variants",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by orders\__show, products\__show, variants\__show

```json
{
  "klass": "products",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by payment_methods\__index

```json
{
  "klass": "payment_methods",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "name": 1
      }
    }
  ]
}
```

#### Used by products\__index

```json
{
  "klass": "products",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "sku": 1
      }
    },
    {
      "key": {
        "company_id": 1,
        "sku_2": 1,
        "sku": 1
      }
    },
    {
      "key": {
        "company_id": 1,
        "sku_3": 1,
        "sku": 1
      }
    },
    {
      "key": {
        "company_id": 1,
        "name": 1,
        "sku": 1
      }
    }
  ]
}
```

#### Used by products\__show

```json
{
  "klass": "variants",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "product_id": 1
      }
    }
  ]
}
```

#### Used by products\__show, stock_messages\__show, variants\__show

```json
{
  "klass": "stock_messages",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "_id": 1
      }
    }
  ]
}
```

#### Used by statuses\__index

```json
{
  "klass": "statuses",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "name": 1
      }
    }
  ]
}
```

#### Used by stock_messages\__index

```json
{
  "klass": "stock_messages",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "name": 1
      }
    }
  ]
}
```

#### Used by variants\__show

```json
{
  "klass": "order_lines",
  "indexes": [
    {
      "key": {
        "company_id": 1,
        "variant_id": 1
      }
    }
  ]
}
```

#### Used by countries\__show, delivery_methods\__show, payment_methods\__show, stock_messages\__show, statuses\__show, variants\__show

```json
{
  "klass": "webshops",
  "indexes": [
    {
      "key": {
        "_id": 1,
        "company_id": 1
      }
    }
  ]
}
```