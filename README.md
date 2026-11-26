<p align="center">
  <a href="https://ag.tavardt.com/pt/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Validador de Robots.txt e Governação de Rastreadores

[![Verificador Robots.txt](https://img.shields.io/badge/TAVARDT-Robots.txt-5b3cf5.svg)](https://tools.tavardt.com/pt/verificador-robots-txt/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

O **TAVARDT Validador de Robots.txt** disponibiliza auditoria automatizada de diretivas de rastreamento, conformidade com a norma RFC 9309 e governação de robôs de inteligência artificial em Portugal.

***

## Arquitetura do Protocolo e Matriz de Governação

Os rastreadores de motores de busca e agentes de inteligência artificial interpretam o robots.txt para determinar os limites de acesso e indexação. Falhas de configuração como bloqueios globais inadvertidos provocam desindexação total e perda de tráfego orgânico.

Esta ferramenta analisa a sintaxe das regras, identifica valores de crawl-delay excessivos, afere políticas de acesso a robôs de IA e valida sitemaps com base em 100 pontos sem dependências externas.

O motor analítico avalia as diretivas de acordo com a norma RFC 9309 e as diretrizes dos motores de pesquisa:

<table>
  <thead>
    <tr>
      <th>Vetor de Governação</th><th>Critério de Auditoria</th><th>Dedução</th><th>Impacto em Rastreio e SEO</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Regra de Disallow Global</strong></td><td>Verifica blocos <code>User-agent: *</code> com <code>Disallow: /</code> desprovidos de regras <code>Allow:</code> compensatórias.</td><td>-50 pts</td><td>Bloqueio crítico que impede motores de busca de indexar todo o portal.</td>
    </tr>
    <tr>
      <td><strong>Declaração de Sitemap XML</strong></td><td>Fiscaliza a presença de pelo menos uma diretiva <code>Sitemap:</code> associada a um feed XML válido.</td><td>-20 pts</td><td>Dificulta a descoberta sistemática e atrasa a indexação de novas publicações.</td>
    </tr>
    <tr>
      <td><strong>Crawl-Delay Excessivo</strong></td><td>Identifica diretivas <code>Crawl-delay</code> superiores a 5 segundos atribuídas de forma genérica.</td><td>-15 pts</td><td>Gargalo severo no orçamento de rastreio em portais com elevado volume de páginas.</td>
    </tr>
    <tr>
      <td><strong>Governação de Bots de IA</strong></td><td>Mapeia permissões para 12 agentes de IA (GPTBot, ClaudeBot, PerplexityBot, etc.), reportando bloqueio ou acesso livre.</td><td>Sinal Analítico</td><td>Protege conteúdos proprietários contra recolha automatizada para treino de modelos.</td>
    </tr>
    <tr>
      <td><strong>Disponibilidade do Servidor</strong></td><td>Verifica código de estado HTTP 200 e estabilidade durante o download do ficheiro.</td><td>Pontuação zerada (0 pts)</td><td>Servidor inacessível impossibilitando a leitura das diretivas pelos motores.</td>
    </tr>
  </tbody>
</table>

### Escala de Governação e Níveis de Estado

O utilitário atribui um índice global de qualidade classificando a conformidade do ficheiro robots.txt:

* <strong>80 a 100 (COMPLIANT)</strong>: Pura conformidade com a RFC 9309; sitemaps declarados, ausência de bloqueios globais e regras consistentes.
* <strong>50 a 79 (WARNING)</strong>: Diretivas funcionais mas com aspetos a corrigir, como falta de sitemap ou delay elevado.
* <strong>0 a 49 (CRITICAL)</strong>: Bloqueio total de motores de pesquisa, inacessibilidade do ficheiro ou regras desastrosas.

***

## Instalação e Execução

Construído exclusivamente com a biblioteca padrão do Python 3.8+, sem qualquer dependência externa.

```bash
git clone https://github.com/TAVARDT-Portugal/robots-txt-validator-pt.git
cd robots-txt-validator-pt
```

### Execução Padrão via CLI

```bash
python robots_validator.py https://exemplo.pt
```

### Saída Estruturada para Pipelines em JSON

```bash
python robots_validator.py https://exemplo.pt -j
```

***

## Conformidade e Integridade Digital em Portugal

A gestão estruturada do ficheiro robots.txt apoia as recomendações de segurança e integridade de ativos web em Portugal. Estabelecer permissões claras previne a indexação de áreas de administração enquanto garante a visibilidade dos conteúdos públicos.

Recomenda-se a inclusão de testes automatizados do robots.txt nos fluxos contínuos de desenvolvimento para garantir uma presença online fiável.

***

## Perguntas Frequentes Técnicas

### Como o validador identifica bloqueios globais de indexação?

O motor avalia blocos com <code>User-agent: *</code>. Caso localize a regra <code>Disallow: /</code> sem nenhuma diretiva compensatória <code>Allow:</code>, o sistema deduz 50 pontos e emite alerta de bloqueio crítico da aplicação.

### Por que a ausência da diretiva Sitemap é penalizada no robots.txt?

Declarar a localização do sitemap no robots.txt orienta diretamente os rastreadores para os feeds oficiais de conteúdo. A ausência da diretiva <code>Sitemap:</code> acarreta penalidade de 20 pontos e gera alerta de otimização.

### Qual é o impacto de um crawl-delay excessivo?

Configurar um <code>Crawl-delay</code> superior a 5 segundos restringe drasticamente o orçamento de rastreamento de portais médios e grandes, atrasando a indexação de novas páginas. Essa configuração gera dedução de 15 pontos.

### Quais robôs de inteligência artificial são monitorados pelo validador?

A auditoria mapeia doze robôs de IA proeminentes: GPTBot, ChatGPT-User, ClaudeBot, Anthropic-AI, PerplexityBot, CCBot, Cohere-AI, Google-Extended, Applebot-Extended, Omgilibot, Diffbot e ByteSpider.

### O que significam as faixas de status e pontuação de governança?

Notas entre 80 e 100 indicam status COMPLIANT sob a RFC 9309. Entre 50 e 79 pontos o status é WARNING por ausência de sitemaps ou delay elevado, e abaixo de 50 pontos o status é CRITICAL, apontando bloqueio severo de rastreamento.

***

## Apoio Técnico e Consultoria Especializada

Para auditorias técnicas de SEO, governação de rastreadores e integridade aplicacional, consulte os especialistas da **TAVARDT**.

***

## Links Úteis

* **Portal Corporativo:** https://ag.tavardt.com/pt/
* **Suíte de Diagnósticos:** https://tools.tavardt.com/pt/
* **Contacto Técnico:** https://ag.tavardt.com/pt/contacto/

***

### Licença
Distribuído sob a Licença MIT.

***

© 2026 TAVARDT. Todos os direitos reservados.
