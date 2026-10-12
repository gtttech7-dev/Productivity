# Focus — Painel de produtividade

Projeto React + Vite, sem login, para organizar tarefas, metas e planejamento pessoal.

## Funcionalidades
- Dashboard com indicadores calculados a partir dos dados.
- Criar, editar, concluir/reabrir e excluir tarefas.
- Busca por tarefas.
- Metas com progresso editável.
- Calendário mensal.
- Categorias iniciais e tema claro/escuro.
- Backup JSON para exportar/importar.
- Permissão e teste de notificação do navegador.
- Manifest e service worker básico para preparar PWA.

## Executar
Requer Node.js LTS. Nesta pasta, rode `npm install` e depois `npm run dev`.

## Build e publicação
Rode `npm run build`. A build fica em `dist`. Na Vercel, comando `npm run build` e diretório `dist`. Use HTTPS.

## Dados
Os dados são salvos no `localStorage` deste navegador. Não existe login ou sincronização entre dispositivos. Limpar os dados do navegador pode removê-los; exporte backups regularmente.

## Notificações
O app pode pedir permissão e testar uma notificação. Ainda não agenda lembretes automáticos nem envia push confiável com o site fechado. Isso exige Firebase Cloud Messaging, service worker configurado para push e backend para programar notificações.

## Firebase futuramente
O armazenamento está isolado em `src/services/storage.js`. Adicione serviços separados para Firebase Authentication e Cloud Firestore, regras de segurança por usuário e migração local com IDs estáveis. Nunca coloque credenciais administrativas no frontend.
