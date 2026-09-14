# 农历 · Dois Calendários

Um conversor bidirecional entre o calendário **gregoriano** e o calendário **chinês lunissolar (农历)**, com datas especiais, curiosidades culturais e suporte a três idiomas.

🔗 **Acesse aqui:** [zhujaxuen.github.io/nongli](https://zhujaxuen.github.io/nongli/)

![status](https://img.shields.io/badge/status-ativo-brightgreen) ![licença](https://img.shields.io/badge/licen%C3%A7a-MIT-blue)

---

## ✨ Funcionalidades

- **Conversão nos dois sentidos** — gregoriano → chinês e chinês → gregoriano, para qualquer ano entre **1901 e 2100**
- **Meses intercalares (闰月)** tratados corretamente, incluindo o cálculo de qual mês vira o mês extra em cada ciclo
- **Ano do zodíaco e ciclo sexagenário** (ex: 己酉 / Galo de Terra), com os 12 animais e os 5 elementos (Wu Xing)
- **Ano chinês contínuo** (黄帝纪年 / calendário do Imperador Amarelo)
- **Datas especiais** — os 7 principais festivais tradicionais chineses, com a data gregoriana recalculada para qualquer ano
- **Card estilo folhinha tradicional (老黄历)** — dia, mês lunar, ano do zodíaco e tags 宜/忌
- **3 idiomas** — 中文 (simplificado), Português e English, com botão de troca no canto superior direito
- **100% estático** — sem backend, sem dependências externas, roda inteiramente no navegador

## 🌐 Idiomas

O idioma inicial é escolhido, em ordem de prioridade:

1. Parâmetro na URL — `?lang=zh` / `?lang=pt` / `?lang=en`
2. Pasta do caminho — `/china/`, `/en/`, `/pt/`
3. Idioma do navegador do visitante
4. Português como padrão

| Idioma | Link direto |
|---|---|
| 🇨🇳 中文 | [/china/](https://zhujaxuen.github.io/nongli/china/) |
| 🇧🇷 Português | [/pt/](https://zhujaxuen.github.io/nongli/pt/) |
| 🇬🇧 English | [/en/](https://zhujaxuen.github.io/nongli/en/) |

## 📁 Estrutura do repositório

```
nongli/
├── index.html       # página principal (detecta o idioma automaticamente)
├── china/index.html # mesma página, abre direto em 中文
├── en/index.html     # mesma página, abre direto em English
└── pt/index.html    # mesma página, abre direto em Português
```

Todos os arquivos são **cópias idênticas** — a lógica de idioma roda inteiramente em JavaScript no navegador, então cada pasta só precisa existir fisicamente para o GitHub Pages servir o `index.html` correspondente.

## 🧮 Como funciona a conversão

O calendário chinês não segue uma fórmula fixa: cada mês começa numa lua nova real (calculada para o horário de Pequim) e a inserção do mês intercalar depende da posição do sol ao longo do ano. Por isso, a conversão usa uma **tabela astronômica pré-calculada** cobrindo 1900–2100, derivada de dados de novilúnios e termos solares.

## 🛠️ Rodando localmente

Não precisa de instalação — é um site estático. Algumas opções:

```bash
# Python
python -m http.server 8000

# Node (via npx)
npx serve
```

Ou use a extensão **Live Server** no VSCode: botão direito em `index.html` → *Open with Live Server*.

## 📄 Licença

MIT — sinta-se livre para usar, adaptar e melhorar.
