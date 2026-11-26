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
2. Em Authentication, habilite o provedor **E-mail/senha**.
3. Crie o Firestore Database.
4. Habilite o Firebase Storage.
5. Copie as credenciais do app Web para o arquivo `.env`, usando os nomes do `.env.example`.
6. Publique o conteúdo de `firestore.rules` nas regras do Firestore e `storage.rules` nas regras do Storage.
7. Na hospedagem, cadastre as mesmas variáveis `VITE_FIREBASE_*` e faça um novo build.

Sem as variáveis Firebase, a interface abre, mas login, mensagens e arquivos não funcionam. Nunca coloque credenciais administrativas ou chaves privadas no frontend.

## Recursos implementados

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
