# Windows Live Messenger Revival

Homenagem independente ao MSN 2009. Não é produto oficial da Microsoft.

## Executar

- npm install
- npm run dev

## Firebase para contas e chat reais

1. Crie um projeto em https://console.firebase.google.com/.
2. Ative Authentication com Email/Password.
3. Crie Firestore Database e Storage.
4. Configure no ambiente de hospedagem as variáveis VITE_FIREBASE_API_KEY, VITE_FIREBASE_AUTH_DOMAIN, VITE_FIREBASE_PROJECT_ID, VITE_FIREBASE_STORAGE_BUCKET, VITE_FIREBASE_MESSAGING_SENDER_ID e VITE_FIREBASE_APP_ID.

Sem essas variáveis, o login real não funciona. Configure regras de segurança do Firestore e Storage antes de abrir ao público. Nunca exponha credenciais administrativas no frontend.

## Estado

Interface responsiva inspirada no MSN 2009; autenticação Firebase; perfis/status; mensagens diretas em tempo real; histórico; envio de arquivos e imagens; emoticons; efeito local de chamar atenção com animação e som. Convites robustos, presença com heartbeat, eventos de chamar atenção sincronizados no destinatário, notificações em segundo plano, winks e chamadas de áudio/vídeo ainda exigem implementação e testes adicionais.