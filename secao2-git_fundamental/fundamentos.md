# 1. Git Pull e Git fetch

O comando **git fetch** para dar uma olhada nas atualizações do repositório remoto sem trazê-las para o seu ambiente local. Ele vai baixar as mudanças feitas por lá, mas sem mexer no seu código ou fazer o merge automático.

Depois de rodar o **git fetch**, você pode usar o comando:

**git diff <branch_local> origin/<branch_remoto>**

Com isso, dá para comparar e ver o que mudou no repositório remoto antes de decidir se quer trazer essas alterações para o seu código com o **git pull**. Assim, você mantém o controle sobre o que entra no seu projeto.