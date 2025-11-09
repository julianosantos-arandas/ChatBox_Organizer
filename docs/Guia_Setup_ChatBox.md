# 🧩 Guia de Setup — VS Code + Obsidian + Git

Este guia resume todos os passos feitos para integrar o **VS Code** e o **GitHub** em um projeto organizado e profissional.

---


   ```

---

## ⚙️  Criar o arquivo `.gitignore`

1. Crie o arquivo `.gitignore` na raiz do projeto.  
2. Adicione o conteúdo principal:
   ```
   docs/Chatbox Organizer/.obsidian/
   __pycache__/
   *.db
   .vscode/
   ```
3. (Opcional) use o modelo completo universal para projetos Python + VS Code.

---

## 🧱 Inicializar e preparar o Git

1. No terminal, dentro da pasta principal:
   ```bash
   git init
   git add .
   git commit -m "🎯 Estrutura inicial + .gitignore configurado"
   ```
2. (Opcional) configurar nome e e-mail:
   ```bash
   git config --global user.name "Juliano Santos"
   git config --global user.email "seu-email@exemplo.com"
   ```

---

## ☁️ Criar e enviar o repositório para o GitHub

1. Criar um novo repositório no GitHub (`Projeto_ChatBox`).  
2. Copiar o link HTTPS e conectar:
   ```bash
   git branch -M main
   git remote add origin https://github.com/seuusuario/Projeto_ChatBox.git
   git push -u origin main
   ```

---

## 🧩 Criar o Workspace no VS Code

1. No VS Code → **File → Add Folder to Workspace...**
   - Adicione `src/`
   - Adicione `docs/Chatbox Organizer/`
   - (Opcional) adicione `data/`
2. **File → Save Workspace As...**
   - Salve como `ChatBox_Organizer.code-workspace` na raiz do projeto.

---

## ⚙️ Editar o `.code-workspace`

1. Abra o arquivo `.code-workspace`.  
2. Cole este conteúdo:

   ```json
   {
     "folders": [
       { "path": "src" },
       { "path": "docs/Chatbox Organizer" },
       { "path": "data" }
     ],
     "settings": {
       "files.exclude": {
         "**/.obsidian": true,
         "**/__pycache__": true,
         "**/.git": true
       },
       "editor.wordWrap": "on",
       "[python]": { "editor.formatOnSave": true }
     },
     "extensions": {
       "recommendations": [
         "ms-python.python",
         "ms-toolsai.jupyter",
         "yzhang.markdown-all-in-one",
         "shd101wyy.markdown-preview-enhanced"
       ]
     }
   }
   ```

---

## 🧠 Testar e usar o Workspace

1. Feche o VS Code e abra **direto o arquivo `.code-workspace`**.  
2. Verifique a lateral:
   ```
   📂 src
   📂 Chatbox Organizer
   📂 data
   ```
3. Pressione `Ctrl + Shift + X` → veja **“Workspace Recommendations”**.  
4. Instale as extensões sugeridas, se desejar.

---

