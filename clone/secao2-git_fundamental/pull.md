# 1.Git Pull

Para trazer as atualizações do repositório remoto utilizamos o comando ***git pull***

**OBS:** Se quiser verificar se tem alterações para fazer antes de fazer o comando **git pull** podemos fazer os seguintes passos:

1. ***git fetch*** para dar uma olhada nas atualizações do repositório remoto sem trazê-las para o seu ambiente local. Ele vai baixar as mudanças feitas por lá, mas sem mexer no seu código ou fazer o merge automático.
```js
git fetch
```

2. ***git diff <branch_local> origin/<branch_remoto>***

Com isso, dá para comparar e ver o que mudou no repositório remoto antes de decidir se quer trazer essas alterações para o seu código com o git pull. Assim, você mantém o controle sobre o que entra no seu projeto.

No meu caso branch_local = master e branch_remoto = master
