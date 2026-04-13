# 📊 Relatórios Ads

**Ferramenta de automação para geração de relatórios de impulsionamento a partir de dados exportados do Meta Ads Manager.**

🔗 **Acesse agora:** [https://evandrofe.github.io/relatorios-ads/](https://evandrofe.github.io/relatorios-ads/)

---

## 🚀 O que é?

O **Relatórios Ads** é uma aplicação web que transforma planilhas brutas exportadas do Gerenciador de Anúncios do Meta (Facebook/Instagram Ads) em relatórios profissionais, prontos para apresentar aos clientes.

O sistema **detecta automaticamente o tipo de campanha** pelo nome, **preenche apenas as métricas correspondentes** e gera um relatório visual com exportação para Excel e PDF — tudo no navegador, sem necessidade de instalação.

---

## ✨ Funcionalidades

- **Importação automática** de arquivos `.xlsx` exportados do Meta Ads Manager
- **Detecção inteligente de objetivos** pelo nome da campanha (com correção automática de erros de grafia)
- **Tela de revisão** para conferência e ajuste dos objetivos antes de gerar o relatório
- **Preenchimento seletivo** — cada tipo de campanha preenche apenas suas métricas relevantes
- **Separação visual por data** — campanhas agrupadas por período para fácil leitura
- **Exportação para Excel** formatado e profissional
- **Exportação para PDF** via impressão do navegador
- **Nome do cliente** extraído automaticamente do nome do arquivo
- **100% client-side** — nenhum dado é enviado para servidores externos

---

## 📋 Padrão de Nomenclatura das Campanhas

Para que a detecção automática funcione corretamente, as campanhas devem seguir o padrão:

```
Nome do Cliente - Formato - DD/MM/AA - Objetivo
```

### Exemplos:
```
Tijotel - Carrossel - 01/03/26 - ALC
Tijotel - Post - 05/03/26 - ENG
Tijotel - Reels - 10/03/26 - WHATS
Tijotel - Post - 12/03/26 - ENG CLIQUE NO LINK
Tijotel - Reels - 15/03/26 - VIEWS
```

---

## 🎯 Tipos de Campanha e Métricas

| Objetivo | Palavras-chave | Métricas Preenchidas |
|---|---|---|
| **Alcance** | `ALC`, `ALCANCE`, `AL` | Alcance + CPM |
| **Engajamento** | `ENG`, `ENGAJAMENTO` | Engajamento¹ + Custo por Interação |
| **Engajamento + Link** | `ENG` + `CLIQUE NO LINK` | Cliques no Link + CPC |
| **Conversas (WhatsApp)** | `WHATS`, `WHATSAPP` | Conversas Iniciadas + Custo por Conversa |
| **WhatsApp + Link** | `WHATS` + `CLIQUE NO LINK` | Cliques no Link + CPC |
| **Reels / Vídeo** | Formato = Reels ou Vídeo | Alcance + Visualização (ThruPlay) + Custo por ThruPlay |

> ¹ Engajamento é preenchido apenas para formatos **Panfleto**, **Carrossel** ou **Virtual**. Para Reels/Vídeo, os dados vão para Visualização (ThruPlay).

---

## 🔄 Regras de Detecção

1. **O objetivo é sempre definido pelo nome da campanha** — o formato (Reels, Carrossel, etc.) é apenas informação visual
2. **Exceção: Reels/Vídeo** — sempre exibe ThruPlay + Alcance + Visualização, independente do objetivo escrito
3. **Abreviações aceitas:** `AL`, `ALC`, `ENG`, `WHATS`, `WAPP`, `TRAF`, `VIEWS`
4. **Correção automática de grafia** — o sistema tolera pequenos erros de digitação (ex: "ALCNACE", "ENGAJAMETO")
5. **Se o sistema não detectar o objetivo**, a tela de revisão permite seleção manual
6. **Validade** — a data é extraída do nome da campanha (não da exportação do Meta)

---

## 📐 Estrutura do Relatório

O relatório final possui **17 colunas**, todas sempre visíveis:

| # | Coluna | Descrição |
|---|---|---|
| A | Nome da Ação | Nome completo da campanha |
| B | Formato | Tipo de mídia (Carrossel, Post, Reels, etc.) |
| C | Validade | Data extraída do nome + espaço para data final |
| D | Investimento | Orçamento da campanha |
| E | Valor Gasto | Valor efetivamente consumido |
| F | Custo por 1.000 Pessoas | CPM (apenas Alcance) |
| G | Custo por Cliques no Link | CPC (apenas Eng+Link / Conv+Link) |
| H | Custo por ThruPlay | Custo por visualização de vídeo (apenas Reels) |
| I | Custo por Interação | Custo por engajamento (apenas Engajamento) |
| J | Custo por Conversa | Custo por conversa iniciada (apenas Conversas) |
| K | Filtro | Segmentação (preenchimento manual) |
| L | Cidade | Localização (preenchimento manual) |
| M | Alcance | Contas alcançadas (Alcance e Reels) |
| N | Visualização | ThruPlay (apenas Reels) |
| O | Engajamento | Interações com o post (apenas Engajamento) |
| P | Conversas Iniciadas | Conversas no WhatsApp (apenas Conversas) |
| Q | Cliques no Link | Cliques em links externos (Eng+Link / Conv+Link) |

---

## 🛠️ Tecnologias

- **HTML5 / CSS3 / JavaScript** — aplicação 100% client-side
- **SheetJS (xlsx.js)** — leitura de arquivos Excel
- **ExcelJS** — geração de Excel formatado
- **GitHub Pages** — hospedagem gratuita

---

## 🔒 Privacidade

Todos os dados são processados **localmente no navegador**. Nenhuma informação é enviada para servidores externos. Os arquivos importados nunca saem do seu dispositivo.

---

## 👨‍💻 Desenvolvedor

**Evandro Ferraz**
Publicista | Designer Digital | Creative Publicidade e Marketing

[![GitHub](https://img.shields.io/badge/GitHub-evandrofe-181717?style=flat&logo=github)](https://github.com/evandrofe)

---

## 📄 Licença

Este projeto é de uso proprietário da Creative Publicidade e Marketing.
