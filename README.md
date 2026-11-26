# Windows Live Messenger Revival

Homenagem independente ao MSN clássico. Não é produto oficial da Microsoft e não utiliza a rede original do MSN.

## Rodar localmente

1. Instale Node.js 20 ou superior.
2. Copie `.env.example` para `.env` e preencha as credenciais do seu projeto Firebase.
3. Execute:

```bash
npm install
npm run dev
```

Para gerar a versão de produção: `npm run build`. O resultado fica em `dist/`.

## Configurar o Firebase

1. Crie um projeto em https://console.firebase.google.com/.
2. Em Authentication → Sign-in method, habilite **Google** (selecione um e-mail de suporte) e, se desejar manter o cadastro tradicional, também **E-mail/senha**.
3. Em Authentication → Settings → Authorized domains, adicione `windows-live-messenger-revival.vercel.app` e `windows-live-messenger-revival-git-main-staelbr1975-4059.vercel.app`.
4. Em Project settings → General, copie a configuração do app Web Firebase para as variáveis `VITE_FIREBASE_*` da Vercel.
5. Crie o Firestore Database.
6. Habilite o Firebase Storage.
7. Publique o conteúdo de `firestore.rules` nas regras do Firestore e `storage.rules` nas regras do Storage.
8. Na Vercel, cadastre as seis variáveis `VITE_FIREBASE_*` em Project → Settings → Environment Variables e faça redeploy.

Sem as variáveis Firebase, a interface abre, mas login, mensagens e arquivos não funcionam. Nunca coloque credenciais administrativas ou chaves privadas no frontend.

## Recursos implementados

- Login com Google (OAuth popup, com alternativa por redirecionamento em navegadores que bloqueiam pop-ups).
- Cadastro e login por e-mail e senha.
- Perfil, mensagem pessoal e estados disponível/ocupado/ausente/invisível.
- Lista de contatos com atualização em tempo real.
- Conversas privadas com histórico e mensagens em tempo real.
- Envio de imagens e arquivos permitidos pelas regras do Storage.
- Emoticons.
- **Chamar a atenção** com tremor e som local e alerta sincronizado para o outro participante enquanto o chat está aberto.
- Layout adaptado para celular e computador.

## Ainda em desenvolvimento

- Fluxo de convite e aceite de contatos (o protótipo atual adiciona por e-mail diretamente).
- Presença com detecção confiável de desconexão e estado invisível privado.
- Notificações do sistema quando a página estiver fechada ou em segundo plano.
- Winks/figurinhas animadas e chamadas de áudio/vídeo.
- Testes de segurança, build e validação em dois dispositivos.

Este é um projeto independente inspirado na experiência visual e em recursos do Messenger antigo. Não é uma restauração do serviço ou protocolo proprietário da Microsoft.
