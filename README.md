<p align="center">
  <img src="./images/icon.png" alt="Logo do Cyberpunk Theme" width="320">
</p>

# Cyberpunk Theme

Tema escuro cyberpunk para VS Code e Cursor, construído com uma paleta vibrante
de cores do Tailwind CSS.

## Mapeamento de cores

| Cor | Hex | Usada em |
|---|---|---|
| zinc-500 | `#71717a` | comentários, linha de número |
| slate-500 | `#64748b` | pontuação, operadores |
| blue-600 | `#2563eb` | chave de objeto (`{ chave: valor }`), acento principal (badges, botões, foco) |
| sky-500 | `#0ea5e9` | funções e chamadas de função, cursor |
| teal-500 | `#14b8a6` | strings |
| green-600 | `#16a34a` | arquivos adicionados no Git |
| amber-500 | `#f59e0b` | números, constantes, booleanos, avisos |
| orange-600 | `#ea580c` | atributos (`class=`, `href=`, etc.) |
| red-400 | `#f87171` | tags HTML/JSX, erros, arquivos deletados no Git |
| pink-400 | `#f472b6` | classes, tipos, interfaces |
| violet-500 | `#8b5cf6` | keywords (`if`, `const`, `function`, etc.) |

Os fundos (editor, sidebar, painéis) usam a escala neutra **Zinc** do Tailwind
(`#09090b`, `#111113`, `#18181b`...) pra combinar com o `zinc-500` que já estava na sua paleta.

Se quiser trocar algum papel (por exemplo, usar `pink-400` pra strings em vez de classes),
é só editar `themes/swatch-dark-color-theme.json` — os blocos em `tokenColors` são
organizados por categoria (comment, string, keyword, function, class, tag, attribute...).

---

## Testar localmente (sem publicar)

Com [Node.js](https://nodejs.org) instalado:

```bash
npm install -g @vscode/vsce
cd cyberpunk-theme
vsce package
```

Isso gera um `cyberpunk-theme-0.1.0.vsix`. Para instalar:

- **VSCode / Cursor:** `Ctrl+Shift+P` → **"Extensions: Install from VSIX..."** → selecione o `.vsix`
  (ou arraste o arquivo pra dentro da janela do editor).

Depois, ative em `Ctrl+Shift+P` → **"Preferences: Color Theme"** → **"Cyberpunk Theme"**.

## Publicar

Antes de publicar, substitua o `publisher` no `package.json` pelo identificador
criado no Visual Studio Marketplace e adicione a URL correta do repositório.

### VS Code Marketplace

```bash
vsce login <seu-publisher>
vsce publish
```

### Open VSX (Cursor)

```bash
npm install -g ovsx
ovsx publish -p <seu-token-open-vsx>
```
