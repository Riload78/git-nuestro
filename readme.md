# Practica Git - Git Nuestro

### ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1

De esta forma vuelvo al commit anterior en el Graph (git reset HEAD~1)

Y además hace un git restore en el working Copy

### ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
Para rehacer el commit he tenido que usar git reflog ya que el commit no era visible
en la lista de commits. 

Con git reflog me muestra todos los cambios realizados.

Luego un git reset 9174b7c para volver al commit y un git restore git-nuestro.md para actualizar el working copy

### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No ha causado ningún conflicto porque se ha mergeado main sobre styled.
La rama styled esta mas avanzada que main. Creo que se trata de un fast forward

### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Si, porque los archivos son diferentes

### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, lo que hizo fue actualizar el archivo git-nuestro.md con os cambios que tenia en la rama styled. 
Ahora la rama main y styled esta iguladas

### ¿Qué comando o comandos utilizaste en el paso 25?
➜ git log --graph
~~~
*   commit a99b712338c36e7850132e42b048b2e5da746df2 (HEAD -> main, styled)
|\  Merge: 9174b7c def83a1
| | Author: Ricardo Lopez <rlopez@next-ecommerce.com>
| | Date:   Tue Dec 5 10:07:59 2023 +0100
| |
| |     Resolve conflict git-nuestro merge htlmlfy
| |
| * commit def83a1a84fad66a3eae36b52eef1df6054ab011 (htmlify)
| | Author: Ricardo Lopez <rlopez@next-ecommerce.com>
| | Date:   Tue Dec 5 09:34:38 2023 +0100
| |
| |     change git-nuestro.md b:htmlify
| |
* | commit 9174b7cb9b02f7ef8edba8cd5832b5cd94535efe
|/  Author: Ricardo Lopez <rlopez@next-ecommerce.com>
|   Date:   Tue Dec 5 08:34:10 2023 +0100
|
|       Change git-nuestro b:styled
|
* commit edfea26d86bd802febfb57414b751f93126ceaf7
  Author: Ricardo Lopez <rlopez@next-ecommerce.com>
  Date:   Tue Dec 5 08:28:30 2023 +0100

      first commit - add git-nuestro.md

~~~

### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí es fast forward. La he cagado y he hecho un git merge title y directamente me ha hecho el fast forward

Tenia que haber ejecutado git merge --no-ff para que hubiera registrado el commit.
He intentado hacer un git merge --abort pero como el commit no se ha registrado no puedo revertirlo
Hago un git reflog para volver al commit del cambio de titulo de la rama title para volver a hacer el proceso

### ¿Qué comando o comandos utilizaste en el paso 27?
git restore <commit>

### ¿Qué comando o comandos utilizaste en el paso 28?
git restore git-nuestro.md desde la rama main

### ¿Qué comando o comandos utilizaste en el paso 29?
➜ git branch -d title desde la rama main

### ¿Qué comando o comandos utilizaste en el paso 30?
➜ git reflog para averiguar el commit en el que merge
daf1644 (main) HEAD@{13}: commit: Change git-nuestro.md b:title
➜ git checkout daf1644

### ¿Qué comando o comandos usaste en el paso 32?
➜ git log
➜ git checkout edfea26d86bd802febfb57414b751f93126ceaf7


### ¿Qué comando o comandos usaste en el punto 33?
➜ git reflog
➜ git checkout daf1644