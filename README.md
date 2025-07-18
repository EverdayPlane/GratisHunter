# GratisHunter

# 🎮 GrátisHunter — Caçador de Jogos Gratuitos

**GrátisHunter** é um bot multiplataforma que rastreia jogos gratuitos nas lojas **Epic Games**, **Steam** e **GOG.com**, envia notificações via Discord com estilo visual (embeds), e exibe um dashboard interativo com histórico, filtros e gráficos. Ideal para quem não quer perder nenhuma oferta!

---

## 🚀 Funcionalidades

- 🔎 Rastreia automaticamente jogos gratuitos nas principais lojas de PC.
- 💬 Envia notificações visuais para canais do Discord (embeds estilizados).
- 📚 Salva o histórico localmente para evitar ofertas repetidas.
- 📤 Exporta histórico para CSV com um clique.
- 📊 Exibe gráficos interativos com estatísticas por loja.
- 🖥️ Dashboard visual com filtro por loja e histórico direto no navegador.

---

## 💻 Tecnologias utilizadas

- **Python 3.10+**
- `Flask` — servidor web e rotas
- `Selenium` + `Webdriver Manager` — scraping da Epic Games
- `Requests` + `BeautifulSoup` — scraping de Steam e GOG
- `Plotly` — gráficos interativos no dashboard
- `Discord Webhook` — envio das notificações
- `Bootstrap` — interface responsiva

---

## 🛠️ Instalação

1. Clone o repositório:

```bash
git clone https://github.com/EverdayPlane/GratisHunter
cd GratisHunter


--Instale os pacotes necessários:--
pip install -r requirements.txt

Configure seu webhook do Discord no arquivo: notificacoes/discord_embed.py → substitua WEBHOOK_URL com sua URL real.

Execute o bot: = > python gratishunter.py

🌐 Rotas disponíveis
Rota	Função
/	Dashboard principal com ofertas atuais
/historico	Exibe o histórico de jogos encontrados
/exportar	Exporta o histórico para CSV
/estatisticas	Exibe gráfico de jogos gratuitos por loja e semana

🧠 Estrutura de diretórios
GrátisHunter/
├── gratishunter.py
├── dados/                     # Histórico JSON + CSV exportado
├── lojas/                     # Scraping por loja
├── notificacoes/             # Envio para Discord + histórico local
├── templates/                # Interface HTML
├── static/                   # Estilo CSS
├── requirements.txt
└── README.md
