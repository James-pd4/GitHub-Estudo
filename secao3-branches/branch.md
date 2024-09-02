# 1.Criar uma branch

- Criar uma nova branch: ***git branch nome-da-branch***

- Mudar para branch crianda: ***git checkout nome-da-branch***

##### Outra forma:

- Criar e mudar para a nova branch: ***git checkout -b nome-da-branch***

- Verificar branches disponíveis: ***git branch***


# 2.Excluir uma branch local
Se você deseja deletar uma branch local (ou seja, no seu repositório local), use o comando:

```bash
git branch -d nome-da-branch
```
***Obs:*** Este comando funciona apenas se a branch que você está tentando excluir já foi mesclada com a branch atual ou com a branch main. Caso contrário, você receberá um erro.

Se você quiser forçar a exclusão da branch, mesmo que ela não tenha sido mesclada, use o seguinte comando:

```bash
git branch -D nome-da-branch
```

Se você deseja deletar uma branch remota (ou seja, no repositório remoto, como no GitHub), use o comando:

```bash
git push origin --delete nome-da-branch
```