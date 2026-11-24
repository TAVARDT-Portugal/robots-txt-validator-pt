# Verificador de Robots.txt

[![Verificador Robots.txt](https://img.shields.io/badge/TAVARDT-Robots.txt-5b3cf5.svg)](https://tools.tavardt.com/pt/verificador-robots-txt/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Auditoria tecnica de ficheiros robots.txt, prevencao de bloqueios acidentais de motores de busca, governanca de rastreadores e diretivas de sitemap.

Desenvolvido e mantido pela divisao de arquitetura semantica e indexacao da **TAVARDT Portugal**.

***

## Capacidades de Auditoria de Robots.txt

* **Detecao de Bloqueios Acidentais**: Alertas criticos contra diretivas que impedem o rastreio legitimo de paginas institucionais.
* **Governanca de Robots de IA e Pesquisa**: Configuracao refinada para motores de busca e agentes autonomos de inteligencia artificial.
* **Ligacao ao Sitemap XML**: Validacao da existencia e integridade do apontador `Sitemap:` no ficheiro.
* **Inspecao de Regras de Diretiva**: Analise de instrucoes `Allow`, `Disallow` e parametros de frequencia `Crawl-delay`.
* **Indice de Eficiencia de Rastreio**: Pontuacao tecnica de 0 a 100 com passos claros de correcao de sintaxe.

***

## Instalacao e Execucao

Requer Python 3.8 ou superior, utilizando exclusivamente a biblioteca padrao.

```bash
git clone https://github.com/TAVARDT-Portugal/robots-txt-validator-pt.git
cd robots-txt-validator-pt
python robots_validator.py https://exemplo.pt
```

Para exportacao em JSON:

```bash
python robots_validator.py https://exemplo.pt -json
```

***

## Plataforma Online de Diagnostico

Para verificar e simular o comportamento de rastreadores:

* **Verificador de Robots.txt Oficial**
* **[Portal Corporativo TAVARDT Portugal](https://ag.tavardt.com/pt/)**

***

## Consultoria em Rastreabilidade e SEO Tecnico

Para projetos corporativos de governanca de robots segundo Padroes Web e Protocolo de Exclusao de Robots, consulte a **TAVARDT Portugal**.

***

© 2026 TAVARDT. Todos os direitos reservados.
