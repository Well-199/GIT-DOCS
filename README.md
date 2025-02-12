# GIT-DOCS

📌 Para criar uma branch local via **CMD** (Prompt de Comando), siga estes passos:

### 1. Abra o **CMD** e navegue até o repositório
Se o seu repositório estiver, por exemplo, em `C:\Projetos\meu-repo`, execute:
```cmd
cd C:\Projetos\meu-repo
```

### 2. Verifique em qual branch você está
```cmd
git branch
```

### 3. Criar uma nova branch
Para criar uma nova branch, use:
```cmd
git branch nome-da-branch
```
Substitua `nome-da-branch` pelo nome desejado.

### 4. Alternar para a nova branch
Para mudar para a branch recém-criada, use:
```cmd
git checkout nome-da-branch
```
Ou, de forma mais direta:
```cmd
git checkout -b nome-da-branch
```
Esse comando **cria e já muda** para a nova branch.

### 5. Confirmar que a branch foi criada e está ativa
```cmd
git branch
```
A branch ativa aparecerá com um **asterisco (`*`)** ao lado.

---

📌 Para verificar todas as branches locais no seu repositório Git, use o seguinte comando no terminal ou prompt de comando dentro do diretório do repositório:

```bash
git branch
```
Se quiser listar também as branches remotas junto com as locais, use:

```bash
git branch -a
```

Caso precise ver mais detalhes sobre cada branch, como a última confirmação feita em cada uma, você pode usar:

```bash
git branch -v 
```

---

📌 Para subir suas alterações da branch local `well_teste` diretamente para a branch remota `develop` sem subir sua branch local, siga estes passos: 

### 1️⃣ **Certifique-se de estar na branch `well_teste`**  
```bash
git checkout well_teste
```

### 2️⃣ **Atualize sua branch com a versão mais recente do repositório remoto (opcional, mas recomendado)**  
```bash
git pull origin develop
```
Isso garante que você tenha as últimas mudanças da `develop` antes de enviar as suas.  

### 3️⃣ **Envie suas alterações para a branch remota `develop`**  
```bash
git push origin well_teste:develop
```
Isso significa: "Pegue o conteúdo da minha branch local `well_teste` e empurre para a branch `develop` no repositório remoto".  

### 4️⃣ **(Opcional) Se precisar apagar sua branch local depois**  
Se você não precisar mais da branch `well_teste`, pode deletá-la localmente com:  
```bash
git branch -d well_teste
```
Se a branch ainda não foi mesclada em `develop` e quiser forçar a remoção, use `-D` no lugar de `-d`. 

---

📌 Padrão da empresa trabalhar sempre em uma branch local de acordo com a Task

### 1️⃣ **Crie uma branch local de acordo com a task**
```cmd
git branch nome-da-branch
```

### 2️⃣ **Atualize sua branch local a partir da develop**
```bash
git pull origin develop
```

### 3️⃣ **Após encerrar a task atualize a develop com sua task**

git pull na develop novamente
```bash
git pull origin develop
```
e agora sim atualiazando a develop com a task
```bash
git push origin well_teste:develop
```

### 4️⃣ **Excluindo uma branch local**

```bash
git branch -d nome-da-branch
```
⚠️ O -d (minúsculo) só permite excluir a branch se todas as alterações já tiverem sido mescladas.

⚠️ Cuidado! NÃO USE O -D (maiúsculo) isso forçará a exclusão, perdendo alterações não salvas.

### 4️⃣ **Confirmando a exclusão**

```bash
git branch
```

---

📌 Quando for necessário o merge use:

```bash
git merge nome-da-branch
```

Se houver conflitos, resolva-os e finalize o merge.

---

#### Seletores para usar na documentação
### 1️⃣ 2️⃣ 3️⃣ 4️⃣ 5️⃣ 6️⃣ 7️⃣ 8️⃣ 9️⃣ 🔟