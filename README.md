# Sistema de Gestão Empresarial

Repositório que reúne os aplicativos do sistema de gestão da empresa (confecção/malharia e loja).
Cada app fica em uma pasta própria e é publicado pelo GitHub Pages. A ideia é que, com o tempo,
os apps sejam interligados (mesma estrutura de dados → mesmo banco).

## Aplicativos

| App | Pasta | Para quê | Link |
|---|---|---|---|
| **CAIXA DA LOJA** | `caixa-da-loja/` | Entradas e saídas diárias da loja, com envio do relatório por WhatsApp | https://guilherme2reis.github.io/Sistema-de-Gestao-Empresarial/caixa-da-loja/ |
| **CAIXA DA MALHARIA** | `caixa-da-malharia/` | Entradas e saídas da malharia; saídas por costureira, fornecedor e conta fixa | https://guilherme2reis.github.io/Sistema-de-Gestao-Empresarial/caixa-da-malharia/ |

## Módulos previstos
Cadastro · Vendas/Pedidos · Custos · Formação de preço · Contas a pagar · Despesas · Financeiro/Fluxo de caixa · Estoque/Produção · Dashboard · Inteligência/IA

## Como os apps funcionam (v1)
- 100% estáticos (HTML + JavaScript), sem servidor e sem login.
- Dados salvos no próprio celular (localStorage). Instaláveis na tela inicial (PWA) e funcionam sem internet.
- Atualizar: editar o arquivo, `git push`, e o app se atualiza sozinho no celular.

## Padrão de dados (para integrar depois)
Lançamento do caixa:
```json
{ "id": "...", "tipo": "E|S", "valor": 15000, "forma": "Pix", "categoria": "",
  "obs": "", "data": "2026-10-30", "hora": "13:19", "criadoEm": "ISO-8601" }
```
`valor` em centavos (inteiro) para evitar erro de arredondamento.
