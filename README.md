# tree-test

A partir des données d'une table MySQL (ici en CSV), construire un JSON "nesté" des catégories et sous-catégories la table "flat_categories".

Il peut y avoir potentiellement des niveaux (sous-catégories) infinies.

# Example

Input:

```
id  parent_id   name
1   NULL        Angines
2   1           Sous-Angine 1
```

```
[
    "id": 1,
    "name": "Angines",
    "children": [
        {
            "id": 2,
            "name: "Sous-Angine 1",
        },
        ...
    ]
]

```

