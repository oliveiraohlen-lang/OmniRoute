# Publicar no Firebase Hosting via GitHub

Os arquivos já estão configurados e enviados para o repositório **`oliveiraohlen-lang/OmniRoute`** na branch **`arena/96b5ae72-omniroute`**, incluindo o `firebase.json` na raiz apontando para `firebase-hosting/public`.

## Opção 1: Conectar direto pelo painel do Firebase (sem terminal)

1. Abra o console do Firebase no navegador:
   `https://console.firebase.google.com/`
2. Selecione seu projeto (ou clique em **Create a project / Criar projeto**).
3. No menu lateral esquerdo, clique em **Build > Hosting** e depois em **Get started (Começar)**.
4. Na etapa de configuração do GitHub, marque **Set up automatic builds and deploys with GitHub** e autorize sua conta GitHub:
   - **Repositório**: `oliveiraohlen-lang/OmniRoute`
   - **Branch**: `arena/96b5ae72-omniroute`
   - **Run a build script before every deploy?**: marque **No (Não)** (o arquivo `firebase-hosting/public/index.html` já está pronto).
5. Salve. O próprio Firebase cria a chave de serviço automática no GitHub e publica o site em:
   `https://<id-do-seu-projeto>.web.app`

---

## Opção 2: Publicar pelo terminal (Firebase CLI)

Se preferir rodar a partir do repositório clonado no seu computador:

```bash
git fetch origin arena/96b5ae72-omniroute
git checkout arena/96b5ae72-omniroute
npm install -g firebase-tools
firebase login
firebase use --add
firebase deploy --only hosting
```
