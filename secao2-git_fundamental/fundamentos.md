# 1. Git Pull e Git fetch

O comando **git fetch** para dar uma olhada nas atualizações do repositório remoto sem trazê-las para o seu ambiente local. Ele vai baixar as mudanças feitas por lá, mas sem mexer no seu código ou fazer o merge automático.

Depois de rodar o **git fetch**, você pode usar o comando:

**git diff <branch_local> origin/<branch_remoto>**

Com isso, dá para comparar e ver o que mudou no repositório remoto antes de decidir se quer trazer essas alterações para o seu código com o **git pull**. Assim, você mantém o controle sobre o que entra no seu projeto.

# 2. Git MV
Com o comando ***git mv*** posso mover ou renomear um arquivo.

***OBS:*** tenho que esta na pasta correta e ter já ter feito push dos arquivos 

**EX1:** Mover um aquivo para uma pasta.

1.Criei a de css
2. fora dessa pasta criei o arquivo index.css
3. Fiz o push desses arquivos
4. colocar o arquivo index.css dentro da pasta css

```js
git mv index.css css/index.css
```

**EX2:** Renomear um aquivo.

1.Criei o arquivo rodapre.css dentro da pasta de css
2. Fiz o push desses arquivos
3. quero renomear o arquivo rodapre para rodape

```js
git mv css/rodapre.css css/rodape.css
```