# Diagramme de classe

![Classes](uml/classes.png)

## Vrai ou faux

Etant donné le diagramme de domaine ci-dessus, les assertions suivantes sont-elles vraies ou fausses ? 
- Etudiant est une classe d’association
  - Faux. `Etudiant` est une classe à part entière associée à la classe `Cours`. Une classe d'association est "suspendue" à une association entre 2 classes ce qui n'est pas le cas de la classe `Etudiant`.
- Un étudiant peut participer à autant de cours qu’il veut
  - Vrai. L'association entre la classe `Etudiant` et la classe `Cours` stipule qu'un étudiant peut être associé à 0 ou plusieurs cours (multiplicité *).
- Plusieurs professeurs peuvent enseigner la même discipline
  - Faux. La multiplicité (1) côté `Professeur` de l'association entre `Professeur` et `Discipline` indique qu'un seul professeur est associé à une discipline.
- Un professeur peut enseigner plusieurs disciplines
  - Vrai. La multiplicité (*) côté `Discipline` de l'association entre `Professeur` et `Discipline` indique qu'un professeur peut être associé à aucune ou plusieures disciplines.
- Un cours peut être enseigner à 2 étudiants
  - Faux. La multiplicité (5..30) côté `Etudiant` de l'association entre `Etudiant` et `Cours` indique qu'au moins 5 étudiants doivent être associés à un cours.
- Un cours peut être enseigner à 20 étudiants
  - Vrai. La multiplicité (5..30) côté `Etudiant` de l'association entre `Etudiant` et `Cours` indique qu'entre 5 et 30 étudiants doivent être associés à un cours.

## Question ouverte

Représentez la même association avec la notation UML « petit losange » 

- Quelles informations perd-on par rapport au diagramme ci-dessus ? 
Dans le cas de ce diagramme UML, nous perderions la vision de la classe `Cours`. En effet, cette classe correspondrait à l'intersection ("petit losange") de l'association n-aire entre les classes `Etudiant`, `Professeur` et `Discipline`.
