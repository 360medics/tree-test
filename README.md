# tree-test

## Brief

A partir des données d'une table MySQL (ici en CSV), construire un JSON "nesté" des catégories et sous-catégories à partir des donnée de la table "flat_categories".

## Contraintes

- Typescript
- Il peut y avoir un nombre infini de niveaux (sous-catégories).
- Il n'y a aucune autre restriction sur la structure du projet, les technos, ou modules externes utilisables.
- Idéalement , le rendu prendra la forme d'un service exportable et réutilisable facilement (dans le contexte d'un projet ou d'une API, par exemple). 

## Example

**Input**

```
id  parent_id   name
1   NULL        Angines
2   1           Sous-Angine 1
```

**Output**

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

