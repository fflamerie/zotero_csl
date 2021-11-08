
# Créer des styles bibliographiques personnalisés CSL : Exercices de style

## Exercice de style 1

_Pour cet exercice, vous travaillez en équipe avec un collègue :_

* _l'un est le conducteur et assure la saisie du code,_
* _l'autre est le navigateur et apporte au conducteur, aide, commentaires et suggestions._

Modifiez le style _Elsevier - Harvard (with titles)_ pour que les **auteurs** soient mis en forme selon les consignes du style Garni.

* Attention, il faut bien considérer à la fois les appels de citation **ET** la bibliographie.
* Attention, certains paramétrages par défaut sont **implicites** : si on souhaite les modifier il ne faut pas seulement modifier la valeur d'un attribut mais ajouter un nouvel attribut avec la valeur appropriée.

---

## Exercice de style 2

_Pour cet exercice, vous travaillez en équipe avec un collègue :_

* _l'un est le conducteur et assure la saisie du code,_
* _l'autre est le navigateur et apporte au conducteur, aide, commentaires et suggestions._

_Si vous avez conservé la même équipe que pour l'exercice 1, vous inversez les rôles._

Modifiez le style _Elsevier - Harvard (with titles)_ pour que les **titres** soient mis en forme selon les consignes du style Garni.

La `macro name="title"` du style est un peu plus complexe que la `macro name="author"`, car elle définit une mise en forme conditionnelle en fonction du type de document. Les conditions sont exprimées dans les éléments enfant de l'élément `choose`.

*   `if` définit la 1ère condition : si le document est une thèse ou un rapport, le titre est affiché, suivi entre parenthèses du type de thèse ou de rapport et de son numéro.
*   `else-if` définissent les autres conditions : si le document, par exemple, est une page web, le titre est affiché, suivi de la mention `[WWW Document]`.
*   `else` définit ce qui s'applique dans tous les autres cas : si le document est d'un autre type que ceux indiqués dans les éléments `if` et `else-if`, le titre est affiché.

---

## Exercice de style 3
Modifiez le style _Elsevier - Harvard (with titles)_ pour que la mise en forme des volumes, numéros et pages pour les articles de revues corresponde aux consignes du style Garni.

---

## Exercice de style 4

```
<citation collapse="citation-number">
    <sort>
      <key variable="citation-number"/>
    </sort>
    <layout vertical-align="sup" delimiter=",">
      <text variable="citation-number"/>
    </layout>
  </citation>
```

Comment les appels de citation sont-ils mis en forme dans ce style?

---

## Exercice de style 5

Modifiez le style _Elsevier - Harvard (with titles)_ pour que la mise en forme des appels de citation corresponde aux consignes du style Garni.

---

## Exercice de style 6

Voici l'élément `bibliography` du style _Elsevier-Harvard (with titles)_.
* Pouvez-vous comprendre le paramétrage défini par chacun des 3 attributs de `bibliography`?
* Quels sont les critères de classement des références dans la bibliographie?
* Quel est le dernier caractère affiché dans une référence bibliographique? Est-il toujours identique? Pourquoi?

```
<bibliography hanging-indent="true" entry-spacing="0" line-spacing="1">
    <sort>
      <key macro="author"/>
      <key macro="issued" sort="descending"/>
    </sort>
    <layout>
      <group suffix=".">
        <text macro="author" suffix=","/>
        <text macro="issued" prefix=" "/>
        <group prefix=". ">
          <text macro="title"/>
          <text macro="container"/>
          <text macro="locators"/>
        </group>
      </group>
      <text macro="access" prefix=". "/>
    </layout>
  </bibliography>
```
---


## Exercice de style 7

Modifiez le style _Elsevier Harvard (with titles)_ pour afficher la date originale selon les consignes du style Garni.

---
