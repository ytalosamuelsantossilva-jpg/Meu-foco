# MEU FOCO – Painel de Disciplina Pessoal (PWA)

Estrutura (site estático, sem build):

    index.html      aplicativo completo
    manifest.json   nome, ícones, cores, tela cheia, atalhos
    sw.js           service worker (funciona offline)
    vercel.json     configuração da Vercel
    icons/          ícones do app

## Publicar na Vercel

Opção A – pelo GitHub (recomendada)
1. Crie um repositório no GitHub e envie todos estes arquivos para a raiz dele.
2. Em vercel.com, clique em Add New > Project e importe o repositório.
3. Em "Framework Preset" deixe "Other". Não precisa de build command nem output directory.
4. Clique em Deploy. Você receberá um endereço https://seu-projeto.vercel.app

Opção B – pelo computador
1. Instale o Node.js e, dentro desta pasta, rode: npx vercel
2. Responda às perguntas (aceite os padrões) e depois rode: npx vercel --prod

A Vercel já entrega o site em HTTPS, requisito para o PWA ser instalável.

## Instalar no Android (Chrome)
1. Abra o endereço do seu projeto no Chrome do celular.
2. Aguarde alguns segundos e toque em "Instalar MEU FOCO" (no fim da tela Início) ou no menu ⋮ > "Instalar app".
3. Confirme. O ícone aparece na tela inicial e o app abre em tela cheia, com tela de abertura.

## Seus dados
- Ficam salvos no próprio aparelho (localStorage) e o app pede ao Android proteção contra limpeza automática.
- Limpar os dados do Chrome ou desinstalar o app pode apagar tudo. Use Exportar backup (tela Início) de vez em quando.
- Celular e computador não sincronizam. Para trocar de aparelho, exporte e importe o backup.

## Atualizar o app
Depois de alterar qualquer arquivo e publicar de novo, mude `CACHE = 'meu-foco-v1'` em sw.js para v2, v3...
O app novo aparece na segunda vez em que for aberto.
