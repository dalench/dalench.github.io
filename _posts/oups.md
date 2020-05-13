---
layout: post
title: Signature d'une permutation
published: true
---

Voici la définition officielle de la signature au programme de MPSI.

**Définition.** Il existe une unique application $\eps$ du groupe symétrique $S_n$ dans $\\{-1,1\\}$ telle que $\eps(\tau)=-1$ pour toute transposition $\tau$ et $\eps(\si\si')=\eps(\si)\eps(\si')$ pour toutes permutations $\si$ et $\si'$.

*Remarque.* En MP, on dira plutôt que la signature est l'unique morphisme non trivial de $S_n$ dans $\\{-1,1\\}$.

L'unicité de la signature est à peu près claire puisque les transpositions engendrent $S_n$. Ainsi, un morphisme de groupe qui est déterminé sur les transpositions est déterminé sur $S_n$ en entier.

En ce qui concerne l'existence, la signature est la plupart du temps définie à l'aide du nombre d'*inversions*[^1] et on montre après coup qu'ainsi définie, elle vérifie bien les conditions données dans la définition officielle au programme.

Mais cette façon de procéder ne semble pas très naturelle et j'ai donc cherche un moyen de prouver l'existence sans faire appel à la notion d'inversion et en utilisant simplement des transpositions. Il s'agit de montrer que si une permutation se décompose de deux manières comme un produit de transpositions, les nombres de transpositions intervenant dans ces deux décompositions ont la même parité. En effet, on peut alors poser $\eps(\si)=(-1)^{T(\si)}$ où $T(\si)$ est le nombre de transpositions intervenant dans une telle décomposition d'une permutation $\si$, puisque la parité de ce nombre $T(\si)$ est une quantité intrinsèque à la permutation $\si$.

Je ne prétends pas que cette démonstration ait quoi que ce soit d'original ; je suis sûr que beaucoup y ont pensé avant moi. Mais, comme je ne l'ai pas trouvée dans la littérature, je me permets d'en faire profiter les personnes intéressées.

**Lemme.** Soient $\tau_1,\dots,\tau_p$ des transpositions dans $S_n$ et $i\in\lb1,n\rb$. Alors il existe des transpositions $\tau_1',\dots,\tau_q'$ dans $S_n$ telles que
* $\tau_1\tau_2\dots\tau_p=\tau_1'\tau_2'\dots\tau_q'$ ;
* $p$ et $q$ ont même parité ;
* les supports de $\tau_1',\dots,\tau_{q-1}'$ ne contiennent pas $i$.

*Remarque.* Le support de la "dernière" transposition $\tau_q'$ peut éventuellement contenir $i$.

*Démo.* Pour simplifier, on considérera que des lettres distinctes désignent des entiers de $\lb1,n\rb$ distincts.

---

On traite déjà le cas de deux transpositions $\tau_1$ et $\tau_2$. Si le support de $\tau_1$ ne contient pas $i$, il n'y a rien à faire.
* Si $\tau_1=(i,j)$ et $\tau_2=(k,l)$, alors

$$\tau_1\tau_2=(i,j)(k,l)=(k,l)(i,j)$$

* Si $\tau_1=\tau_2=(i,j)$, alors

$$\tau_1\tau_2=(i,j)(i,j)=\ident$$

L'identité est une composée de "zéro" transposition.

* Si $\tau_1=(i,j)$ et $\tau_2=(i,k)$, alors

$$\tau_1\tau_2=(i,j)(i,k)=(j,i,k)=(k,j,i)=(k,j)(j,i)$$

* Si $\tau_1=(i,j)$ et $\tau_2=(j,k)$, alors

$$\tau_1\tau_2=(i,j)(j,k)=(i,j,k)=(j,k,i)=(j,k)(k,i)$$

---
