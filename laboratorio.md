# Laboratório Prático – Git e GitHub

## Passo a Passo do Laboratório

---

### 1. Configuração Inicial do Git

Antes de começar, configure seu nome e e-mail no Git (substitua pelos seus dados):

```bash
git config --global user.name "Seu Nome"
```
![Captura de tela 2025-05-16 233821](https://github.com/user-attachments/assets/23d9304e-266c-44e6-9b49-4bf590659a23)


```bash
git config --global user.email "seu.email@example.com"
```
![Captura de tela 2025-05-16 233821](https://github.com/user-attachments/assets/642fc726-da0c-4616-9c70-0266189fb686)
![Captura de tela 2025-05-16 233906](https://github.com/user-attachments/assets/4ce1faa7-fede-4cb9-9e79-f2f6061f97bb)

---

### 2. Criar um Repositório Local

Crie uma pasta para o projeto e entre nela:

```bash
mkdir meu-projeto
cd meu-projeto
```
![Captura de tela 2025-05-16 234311](https://github.com/user-attachments/assets/cd78f42c-d7d3-4ae0-b055-fc9842a958dd)

Inicialize um repositório Git:

```bash
git init
```
![Captura de tela 2025-05-16 234336](https://github.com/user-attachments/assets/9ffaf33c-a109-4ccb-8d62-6846f7badd55)

---

### 3. Adicionar Arquivos e Fazer Commit

Crie um arquivo `README.md`:

```bash
echo "# Meu Projeto" > README.md
```
![Captura de tela 2025-05-16 234558](https://github.com/user-attachments/assets/48de35c8-e19c-4ff2-89d9-48caf9386af6)

Verifique o status do repositório:

```bash
git status
```
![Captura de tela 2025-05-16 234626](https://github.com/user-attachments/assets/6f5bf710-3799-4324-8d07-11aee9f7c3d1)

Adicione o arquivo ao staging area:

```bash
git add README.md
```
![Captura de tela 2025-05-16 234656](https://github.com/user-attachments/assets/0a6647c6-ac75-4d50-aaed-46bdfb05f534)

Faça o primeiro commit:

```bash
git commit -m "Primeiro commit: adiciona README.md"
```
![Captura de tela 2025-05-16 234743](https://github.com/user-attachments/assets/a7a599e7-4021-4510-8e55-12338de90200)

---

### 4. Criar um Repositório no GitHub

1. Acesse o GitHub e clique em **New repository**.  
2. Nomeie como `meu-projeto`, deixe público e **não** adicione arquivos automáticos (README, .gitignore, etc.).  
3. Copie a URL do repositório, por exemplo:

```text
https://github.com/seu-usuario/meu-projeto.git
```
![Captura de tela 2025-05-17 003421](https://github.com/user-attachments/assets/baedd5f4-0ead-400f-8dee-2287153d0912)

---

### 5. Conectar o Repositório Local ao GitHub

Adicione o repositório remoto:

```bash
git remote add origin https://github.com/seu-usuario/meu-projeto.git
```
![Captura de tela 2025-05-16 235719](https://github.com/user-attachments/assets/189c51d9-0196-49a0-af63-ccc5ac06b149)

Envie as alterações para o GitHub:

```bash
git push -u origin main
```
![Captura de tela 2025-05-17 000731](https://github.com/user-attachments/assets/6047b879-f253-41bf-8f17-b44cbc894739)

> **ATENÇÃO:** Nesse passo você será solicitado a autenticar com seu usuário GitHub e um Personal Access Token.

![Captura de tela 2025-05-17 001230](https://github.com/user-attachments/assets/8d1bc907-5cb4-4fb2-bd69-dd2bdc02cee8)

---

### 6. Criar e Trabalhar em uma Nova Branch

Crie e mude para a branch de feature:

```bash
git checkout -b feature/nova-funcionalidade
```
![Captura de tela 2025-05-17 001230](https://github.com/user-attachments/assets/7e0e4f53-de6b-4070-9ebe-f0297ef71e71)

Crie um arquivo de exemplo:

```bash
echo "Nova funcionalidade em desenvolvimento" > nova-funcionalidade.txt
```
![Captura de tela 2025-05-17 001330](https://github.com/user-attachments/assets/cc7838e5-80d4-407c-b8d1-c1382fbfd4d2)

Adicione e faça commit:

```bash
git add nova-funcionalidade.txt
git commit -m "Adiciona nova funcionalidade"
```
![Captura de tela 2025-05-17 001330](https://github.com/user-attachments/assets/cc7838e5-80d4-407c-b8d1-c1382fbfd4d2)

Envie a branch ao GitHub:

```bash
git push -u origin feature/nova-funcionalidade
```
![Captura de tela 2025-05-17 001330](https://github.com/user-attachments/assets/cc7838e5-80d4-407c-b8d1-c1382fbfd4d2)

---

### 7. Fazer Merge da Branch na Main

Volte para a `main`:

```bash
git checkout main
```

Atualize a `main` com as últimas alterações:

```bash
git pull origin main
```

Mescle a feature na `main`:

```bash
git merge feature/nova-funcionalidade
```

Envie o merge final:

```bash
git push origin main
```
![Captura de tela 2025-05-17 004428](https://github.com/user-attachments/assets/0955767d-8531-4ae8-8016-a753c8f9fc42)
