---
sidebar_position: 2
---

# Documentation Admin

Vous faites partie de l'équipe d'Administration de **New Dawn** et vous cherchez des infos pour vous sortir d'un bourbier immense ou simplement pour aider notre magnifique et ingénieux Responsable Dev' qu'est **Lexinor**, vous êtes tombé au bon endroit !

## Informations Générales

**----- TODO -----**

### Créer un item

Tout notre système d'inventaire utilise un script créé par l'équipe d'[Overextended](https://github.com/overextended). Le script en question est l'[Ox_Inventory](https://overextended.github.io/docs/ox_inventory), heuresement pour nous l'équipe d'**OX** a créé une belle documentation disponible ici : [Documentation](https://overextended.github.io/docs/)
Sur ce site vous pourrez y retrouver toutes les informations nécessaires concernants tous les scripts de cette équipe mais ici on se concentrera sur la partie qui concerne leur inventaire, [Ox_Inventory](https://overextended.github.io/docs/ox_inventory).

Pour vous simplifier le boulot, je vais vous résumer ici ce dont vous avez besoin pour nous aider à créer n'importe quel item que vous souhaitez, en sachant que vous ne pourrez pas forcément allez trop loin car une partie concerne exclusivement la partie Dev.

Pour créer un item c'est très simple. Il suffit de simplement définir plusieurs informations, voici un exemple ci-dessous :

```
['burger'] = {
    label = 'Burger',
    weight = 220,
    stack = true,
    close = true,
    client = {
        status = { hunger = 200000 },
        anim = { dict = 'mp_player_inteat@burger', clip = 'mp_player_int_eat_burger_fp' },
        prop = {
            model = 'prop_cs_burger_01',
            pos = { x = 0.02, y = 0.02, y = -0.02},
            rot = { x = 0.0, y = 0.0, y = 0.0}
        },
        usetime = 2500,
    }
}
```

Ne vous en faite pas je vais vous expliquer rapidement à quoi corresponds chaque partie, tout sera beaucoup plus clair après ça. 
Pour faire très simple voici une description de chaque informations que vous voyez au dessus.

- ['burger'] : *(Valeur Obligatoire)* Corresponds tout simplement au nom de l'item au niveau du système, vous utiliserez ce nom pour vous give cet item dans vos commandes. Par exemple : /giveitem me burger
- label : *(Valeur Obligatoire)* Corresponds à la valeur affichée dans l'inventaire. Vous pouvez choisir ce que vous voulez et elle peut être différente de la valeur du dessus. Ce ne sera que pour de l'affichage.
- weight : *(Valeur Obligatoire)* Le poids d'une unité de l'item. *Cette valeur est en grammes*
- stack : *(Valeur Obligatoire)* Est-ce que l'item est empilable. On la défini avec : **true** ou **false**
- degrade : *(Valeur Optionnelle)* Chiffre qui corresponds au nombre de minute avant que l'item se dégrade
- close : *(Valeur Optionnelle)* Tout simplement une valeur pour dire si on ferme l'inventaire lorsqu'on utilise l'item. On la défini avec : **true** ou **false**
- description : *(Valeur Optionnelle)* La description de l'objet
- consume : *(Valeur Optionnelle)* Combien d'item sera utilisé lors de l'utilisation de celui ci.
- allowArmed : *(Valeur Optionnelle)* Est-ce qu'on peut utiliser l'item en étant armé. On la défini avec : **true** ou **false**
