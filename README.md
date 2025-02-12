# GIT-DOCS

Para subir suas alterações da branch local `well_teste` diretamente para a branch remota `develop` sem subir sua branch local, siga estes passos: 

Para verificar todas as branches locais no seu repositório Git, use o seguinte comando no terminal ou prompt de comando dentro do diretório do repositório:

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
