# NICE · Business & Legal English

(No código, o app ainda usa o nome interno `Elle`; isso não aparece na tela.)

## Como abrir
Dê dois cliques em `index.html`. Ele abre no navegador; prefira o Chrome ou o Edge, que têm mais vozes femininas. Não precisa instalar nada.

- O progresso fica salvo no próprio navegador. Use Ajustes → Backup para exportar e importar.
- As fontes vêm do Google Fonts. Sem internet, o app continua funcionando, só com uma fonte parecida.
- No celular: depois de publicar o app (Fase 5), dá para "Adicionar à tela inicial" e ele funciona como um app instalado.

## O que já existe
- **6 unidades, 30 lições, 185 termos**, sempre com o grau de equivalência PT ↔ EN:
  1. Fundamentos
  2. Anatomia de um contrato
  3. Linguagem contratual
  4. Societário
  5. M&A
  6. Reuniões e negociação
- **Exercícios:** card de termo novo, múltipla escolha, completar a cláusula, associar pares, tradução, **ache o erro** (30 frases), **ditado** e **fala**
  - O ditado só aparece se o navegador tiver voz em inglês.
  - A fala usa o microfone e o reconhecimento de voz do Chrome/Edge, que precisa de internet. Se o microfone for bloqueado, é só pular. Os dois podem ser desligados em Ajustes.
- **Nivelamento** adaptativo, com até 15 perguntas, que libera as unidades certas
- **Revisar:** repetição espaçada. Erros voltam no mesmo dia e acertos voltam em 1, 3, 7… dias
- **Glossário:** busca e filtros por equivalência e por unidade
- **Ajustes:** voz feminina (americana ou britânica), velocidade, nivelamento, backup
- XP e sequência de dias (com 1 congelamento grátis por semana)

## Estúdio com IA (Gemini, grátis)
1. Entre em aistudio.google.com com sua conta Google → **Get API key** → **Create API key**.
2. No app: **Ajustes → Inteligência artificial** → cole a chave → **Salvar** → **Testar**.

Com a chave configurada, você ganha:
- **Prática extra:** exercícios inéditos sobre o que você já estudou. Também aparece como botão no fim de cada lição.
- **Plain English:** você reescreve uma cláusula em legalese e recebe nota em clareza, precisão jurídica e concisão, mais uma sugestão de versão.
- **Roleplay:** 4 cenários (cliente estrangeiro, negociação de SPA, reunião de conselho, call de próximos passos), com dicas a cada mensagem e um feedback final.
- **Correção de tradução:** quando o app recusar uma tradução sua, o botão "Pedir para a IA avaliar" pede uma segunda opinião.

Cuidados:
- A chave fica só neste navegador e não entra no backup.
- No plano gratuito, o Google pode usar o que você enviar para melhorar os serviços dele. Não envie documentos reais ou confidenciais.
- O modelo padrão é `gemini-3.5-flash-lite`, que é rápido. Para respostas mais elaboradas, mas uns 15 segundos mais lentas, use `gemini-3.5-flash` em Ajustes. O Google aposenta modelos de tempos em tempos: se aparecer "modelo não disponível", apague o campo Modelo e salve para voltar ao padrão.

## Como adicionar conteúdo
Cada unidade fica num arquivo em `js/content/`. O formato está explicado em `_helpers.js`. Rode `tests.html` para conferir se o conteúdo novo está válido.

## Sincronização com o Google Drive (pronta, aguardando publicação)
O código já está pronto. Ele salva o progresso e a chave da IA numa pasta oculta do seu Drive, à qual só o NICE tem acesso, e funciona em qualquer aparelho depois do login com o Google. Para ligar, faltam dois passos, que só funcionam com o app publicado num endereço https (o Google não permite login abrindo o arquivo direto):
1. Publicar o app (recomendado: GitHub Pages, grátis).
2. Criar um "OAuth Client ID" no Google Cloud para esse endereço e colocá-lo em `js/config.js`.

Até lá, a chave da IA fica salva no navegador onde você colou: basta colar uma vez em cada navegador.

## Fase pendente
5. Sincronização com o Google Drive e publicação online
