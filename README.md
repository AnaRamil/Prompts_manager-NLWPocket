# Prompts Manager - NLW Pocket Iniciantes

Este é um pequeno gerenciador de _prompts_ (textos para copy/paste) construído com HTML, CSS e JavaScript puros. O projeto fornece uma interface simples para criar, salvar, buscar, copiar e remover prompts. Os dados são salvos no navegador usando `localStorage`.

---

## Estrutura do projeto

- `index.html` — página principal e layout do app.
- `style.css` — estilos do projeto.
- `script.js` — lógica do app (manipulação de DOM, persistência em localStorage, handlers de botões).
- `assets/` — ícones, imagens e favicon usados pela página.

---

## Funcionalidades

- Criar novo prompt (título + conteúdo).
- Salvar prompt (persistência usando `localStorage`).
- Buscar prompts pelo título (campo de busca na sidebar).
- Selecionar prompt da lista para editar/exibir.
- Remover prompt da lista.
- Copiar conteúdo do prompt para a área de transferência.
- Abrir e colapsar a sidebar para navegar entre prompts.

---

## Requisitos

Você só precisa de um navegador moderno (Chrome, Edge, Firefox, Safari) para abrir o projeto. Para rodar via servidor local (recomendado para evitar problemas com caminhos relativos e políticas de CORS), tenha uma das seguintes opções instaladas: `Python`, `Node.js` (opcionalmente `npx serve`), ou use a extensão Live Server do VS Code.

---

## Como rodar e visualizar o portfolio (opções)

1. Abrir diretamente no navegador (mais simples)

- Navegue até a pasta do projeto e dê um duplo clique em `index.html` para abri-lo no navegador.

2. Usar o Live Server (VS Code)

- Abra a pasta do projeto no VS Code.
- Instale a extensão "Live Server" (se ainda não tiver).
- Clique com o botão direito em `index.html` e selecione "Open with Live Server".

3. Rodar um servidor HTTP simples com Python (Windows PowerShell)

- Abra o PowerShell na pasta do projeto e execute um dos comandos abaixo:

```powershell
# Python 3
python -m http.server 8000

# ou (se usar python3 alias)
python3 -m http.server 8000
```

- Em seguida abra no navegador: `http://localhost:8000`

4. Usar um servidor Node (opcional)

- Com `npx` disponível, você pode usar `serve` ou `http-server`:

```powershell
npx serve .
# ou
npx http-server -p 8000
```

- Depois abra `http://localhost:5000` (ou `:8000`) conforme o retorno do comando.

---

## Uso (rápido)

1. Criar novo prompt: clique em "Novo prompt" na sidebar.
2. Preencher o título (campo editável) e o conteúdo (campo editável abaixo).
3. Salvar: clique em "Salvar" (o prompt será persistido no `localStorage`).
4. Buscar: use o campo de busca na sidebar para filtrar por título.
5. Selecionar: clique em um item da lista para carregar no editor.
6. Copiar: quando um prompt estiver carregado, clique em "Copiar" para enviar o texto para a área de transferência.
7. Remover: clique no ícone de lixeira ao lado de um item na lista para removê-lo.

---

## Resetar / Limpar dados do `localStorage`

Se quiser limpar todos os prompts salvos:

1. Abra as Ferramentas de Desenvolvedor do navegador (F12).
2. Vá até o painel Application / Storage -> Local Storage -> selecione o domínio `file://` ou `localhost`.
3. Remova a chave `prompts_storage` ou execute no console:

```javascript
localStorage.removeItem("prompts_storage")
```

Isso resetará o aplicativo para o estado inicial.

---

## Compatibilidade e notas

- O app usa a API de Clipboard do navegador para copiar texto; navegadores antigos podem não suportar essa API.
- O projeto é intencionalmente simples (sem bundler). Serve como um exemplo de SPA leve sem dependências.

---

## Desenvolvimento e personalização

- Para alterar placeholders, textos ou estilos, edite `index.html` e `style.css`.
- Para mudar comportamento (por exemplo, alterar a chave do `localStorage` ou adicionar timestamp), edite `script.js`.

---

## Licença

Este projeto esta licenciado por "https://github.com/rocketseat-education".

---
