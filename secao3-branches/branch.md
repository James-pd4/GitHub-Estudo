# 1.Criar uma branch

- Criar uma nova branch: ***git branch nome-da-branch***

- Mudar para branch crianda: ***git checkout nome-da-branch***

##### Outra forma:

- Criar e mudar para a nova branch: ***git checkout -b nome-da-branch***

- Verificar branches disponíveis: ***git branch***

# 2.Trazendo o conteúdo de uma branch para outra

Como exemplo vamos simular que queremos trazer os contúdos da branch teste para master

```bash
# Certifique-se de que todas as alterações estão commitadas na branch `teste`
git add .
git commit -m "Descrição das alterações"

# Troque para a branch `master`
git checkout master

# Atualize a branch `master` com as últimas mudanças (opcional)
git pull origin master

# Mescle a branch `teste` na branch `master`
git merge teste

# Resolver conflitos (se houver), depois commit
git add arquivo_conflitante
git commit

# Envie as alterações para o repositório remoto
git push origin master

```


# 3.Excluir uma branch local
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

# 4.Comando stash

O comando git stash é uma ferramenta útil no Git que permite salvar temporariamente as mudanças não commitadas no seu repositório de trabalho, para que você possa trabalhar em outra coisa sem perder o trabalho em andamento. É como colocar suas alterações em uma "prateleira" temporária.

***Obs:*** para usar o comando git stash, antes temos que add as mudanças.

#### Para que serve:

- **Interromper o trabalho atual:** Quando você está trabalhando em uma tarefa, mas precisa mudar de contexto (por exemplo, mudar para outra branch para corrigir um bug urgente), pode usar o git stash para guardar as mudanças inacabadas e voltar a um estado limpo.

- **Manter o repositório limpo:** Permite que você limpe seu ambiente de trabalho (workspace) sem precisar fazer commits de código incompleto ou instável.

#### Como usar o git stash:

#### 1.Guardar as alterações no stash

- **simples:**

```bash
git stash
```
Esse comando guarda todas as suas mudanças não commitadas (arquivos modificados e não monitorados) no stash e restaura o seu diretório de trabalho para o estado do último commit.

- **Com mensagem:**

```bash
git stash save "Mensagem explicativa"
```
Esse comando permite que você adicione uma mensagem ao stash, o que pode ser útil para identificar o stash mais tarde.

#### 2.Ver os stashes disponíveis

```bash
git stash list
```
Isso exibirá uma lista de todos os stashes que você criou, com um índice e a mensagem associada (se houver).

#### 3.Aplicar o stash de volta ao seu diretório de trabalho

- **Simples:**
```bash
git stash apply
```
Esse comando aplica o stash mais recente ao seu diretório de trabalho, mas mantém o stash na lista.

- **Aplicar um stash específico:**
```bash
git stash apply stash@{index}
```
Onde index é o número do stash que você deseja aplicar.

- **Aplicar e remover do stash:**
```bash
git stash pop
```
Esse comando aplica as alterações do stash mais recente e remove-o da lista de stashes.

#### 4.Excluir um stash específico

```bash
git stash drop stash@{index}
```
Esse comando remove um stash específico da lista.

#### 5.Limpar todos os stashes


```bash
git stash clear
```
Esse comando remove todos os stashes armazenados.