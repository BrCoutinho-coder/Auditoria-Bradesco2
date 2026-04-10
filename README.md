# 🏥 Motor Analítico de Conciliação Financeira (Serverless)

Este projeto foi desenvolvido para resolver um dos maiores gargalos operacionais no faturamento hospitalar: o cruzamento de repasses e prevenção de glosas entre o ERP interno (Korus) e a operadora (Orizon/Bradesco).

## 🎯 O Problema
Auditorias manuais levam horas, são suscetíveis a falhas humanas e não dão clareza imediata sobre o **Valor Financeiro em Risco**. Diferenças invisíveis de formatação (espaços, caracteres especiais) nas senhas e datas geram falsos positivos, atrasando o recurso de glosas.

## 🚀 A Solução
Desenvolvi um Web App *Client-Side* que processa a volumetria inteira em segundos, diretamente no navegador.

### Diferenciais Técnicos:
* **Zero Custo de Infraestrutura:** Arquitetura Serverless. Roda 100% no navegador (Client-Side).
* **LGPD Compliant:** Como não há banco de dados na nuvem, os dados sensíveis dos pacientes nunca saem da máquina do faturista.
* **Memória Persistente:** Utilização de `localStorage` para manter um banco de dados interno (DEPARA) de códigos de exames, que aprende e se atualiza a cada novo upload.
* **Motor de Trituração Alfanumérica (Regex):** Algoritmos que higienizam dados brutos (espaços fantasmas, datas corrompidas do sistema) antes do cruzamento lógico.
* **Dashboard Financeiro Reativo:** Integração com `Chart.js` para atualizar KPIs de volume e valores financeiros (R$) em tempo real com base em filtros multicritério.

## 🛠️ Tecnologias Utilizadas
* HTML5, CSS3, JavaScript Vanilla (ES6)
* SheetJS / PapaParse (Processamento de planilhas)
* Chart.js (Visualização de dados)
* GitHub Pages (Deploy)
