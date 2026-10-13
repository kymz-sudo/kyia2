# Íris — IA local com aprendizado controlado

Esta versão é independente de OpenAI e de APIs de IA pagas. Usa WebLLM para executar um modelo no navegador, quando o navegador/dispositivo suporta WebGPU.

## Importante
- O primeiro download do modelo pode ter centenas de MB ou mais, conforme o modelo selecionado.
- A disponibilidade e a velocidade dependem do navegador, WebGPU, RAM e espaço livre.
- Modelos locais menores podem errar mais do que serviços de IA maiores.
- O código não salva histórico de conversa após recarregar. Memórias explícitas ficam em `localStorage` neste navegador.
- “Aprender” aqui significa salvar fatos/preferências e incluí-los no contexto; não significa retreinar os parâmetros do modelo.
- A busca online consulta a API pública da Wikipedia em português. Não reúne literalmente toda a web.

## Como usar no celular
A página deve ser servida por HTTPS para que WebGPU/PWA funcionem melhor. Não basta abrir o arquivo local em alguns navegadores.

### Publicação gratuita
1. Baixe e extraia o ZIP.
2. Crie um repositório no GitHub.
3. Envie `index.html` para a raiz do repositório.
4. Em Settings → Pages, habilite a publicação da branch principal, pasta raiz.
5. Abra a URL HTTPS no Chrome Android.
6. Toque em “Carregar cérebro” e aguarde o download inicial.
7. Se suportado, use o menu do Chrome → “Adicionar à tela inicial”.

Os serviços de hospedagem podem alterar limites e condições. A aplicação não usa chave de API paga, mas o download e as buscas usam internet.

## Modelos
O seletor contém IDs de modelos para WebLLM. Se algum ID não estiver disponível na versão atual da biblioteca, selecione outro modelo compatível ou atualize o ID conforme o catálogo do WebLLM.

## Privacidade
- As mensagens da conversa ficam apenas na memória da página.
- As memórias ficam no armazenamento local do navegador até você apagá-las.
- As consultas de pesquisa são enviadas à API pública da Wikipedia.
- O modelo e a biblioteca são baixados de infraestrutura externa na primeira utilização.
- Não insira informações secretas em memórias se outras pessoas usam o mesmo perfil do navegador.

## Arquivos
- `index.html`: interface, inferência local, busca e memória.
