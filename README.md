# Verificador de Robots.txt

[![Verificador Robots.txt](https://img.shields.io/badge/TAVARDT-Robots.txt-5b3cf5.svg)](https://tools.tavardt.com/pt/verificador-robots-txt/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Ferramenta de governanca de rastreio web em Portugal, inspecionando diretivas de robots.txt, prevenindo esgotamento de crawl budget e protegendo rotas privadas.

Desenvolvido e mantido pela divisao de indexacao web e normas digitais da **TAVARDT Portugal**.

***

## Capacidades de Auditoria de Robots.txt

* **Deteção de Bloqueios Acidentais**: Alertas criticos contra diretivas que impedem o rastreio legitimo de paginas institucionais.
* **Governanca de Robots de IA e Pesquisa**: Configuracao refinada para motores de busca e agentes autonomos de inteligencia artificial.
* **Ligacao ao Sitemap XML**: Validacao da existencia e integridade do apontador `Sitemap:` no ficheiro.
* **Inspeção de Regras de Diretiva**: Análise de instrucoes `Allow`, `Disallow` e parametros de frequencia `Crawl-delay`.
* **Indice de Eficiencia de Rastreio**: Pontuacao tecnica de 0 a 100 com passos claros de correcao de sintaxe.

***

## Instalação e Execucao

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
* **[Portal Corporativo TAVARDT](https://ag.tavardt.com/pt/)**

***

## Consultoria em Rastreabilidade e SEO Tecnico

Para projetos corporativos de governanca de robots segundo Padroes Web e Protocolo de Exclusao de Robots, consulte a **TAVARDT**.

***



## Links Úteis

* **Portal Corporativo:** https://ag.tavardt.com/pt/
* **Suíte de Diagnósticos:** https://tools.tavardt.com/pt/
* **Contacto Técnico:** https://ag.tavardt.com/pt/contacto/

***

### Licença
Distribuído sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter detalhes completos.

***

© 2026 TAVARDT. All rights reserved.
