# GS2026.1 - Prompt and Artificial Intelligence
# ARIA / Mission Control AI
## Equipe:

Enzo Stahal Freitas - RM: 569001

Matheus Bruno de Lima - RM: 572944
 
## Sobre o Projeto:
O objetivo do projeto é monitorar condições operacionais de uma missão espacial experimental, analisando informações relacionadas à temperatura dos módulos, energia, comunicação e status operacional da nave.
A solução utiliza conceitos de programação, algoritmos e inteligência artificial generativa para gerar alertas automáticos e auxiliar na tomada de decisão diante de situações críticas.
 
## Objetivo:
Desenvolver um sistema capaz de:
- Gerar dados simulados dos sensores da missão
- Monitorar dados operacionais em tempo real
- Identificar situações críticas automaticamente
- Gerar alertas com níveis de severidade (CRÍTICO / AVISO / OK)
- Auxiliar na tomada de decisão com ações automatizadas
- Analisar e interpretar os dados com IA generativa
## Funcionalidades
 
### MONITORAMENTO
O sistema gera e monitora automaticamente:
- Temperatura do módulo principal (°C)
- Temperatura do módulo de propulsão (°C)
- Temperatura do módulo de energia (°C)
- Nível de bateria (%)
- Geração de energia solar (W)
- Qualidade do sinal de comunicação (%)
- Status individual de cada módulo operacional (Propulsão, Suporte de vida, Navegação, Comunicação, Energia)
### ALERTAS AUTOMÁTICOS
O sistema identifica e classifica:
- Temperatura crítica no módulo principal (> 85°C)
- Temperatura crítica no módulo de propulsão (> 95°C)
- Energia da bateria crítica (< 15%)
- Energia da bateria baixa (< 30%)
- Geração solar insuficiente (< 50W)
- Falha de comunicação crítica (sinal < 35%)
- Comunicação instável (sinal < 70%)
- Falha ou degradação em qualquer módulo operacional
### TOMADA DE DECISÃO
O sistema realiza ações automatizadas como:
- Emissão de alerta CRÍTICO com intervenção imediata (qualquer parâmetro em nível crítico)
- Emissão de alerta de AVISO com monitoramento reforçado (parâmetros em nível de atenção)
- Manutenção da operação nominal (todos os sistemas dentro dos parâmetros normais)
### ANÁLISE COM IA GENERATIVA
O sistema envia todos os dados e alertas para o modelo **Llama 3.2 1B** (via Ollama), que:
- Gera um diagnóstico geral da missão em linguagem natural
- Identifica os principais riscos operacionais
- Recomenda ações específicas para a equipe de controle
## Relação com Inteligência Artificial
Utilizamos IA generativa com o modelo Llama 3.2 1B rodando localmente via Ollama no Google Colab. O sistema conta com duas camadas de inteligência: uma **IA baseada em regras** (estruturas condicionais if/elif/else) para geração de alertas automáticos e tomada de decisão imediata, e um **modelo de linguagem** (LLM) que recebe os dados estruturados e produz análises e recomendações em linguagem natural. A combinação das duas abordagens permite tanto respostas rápidas e determinísticas quanto análises contextuais mais ricas.
 
## Tecnologias Utilizadas
- **Python** (linguagem de programação)
- **Google Colab** (ambiente de execução)
- **Ollama** (servidor local para execução do modelo de IA)
- **Llama 3.2 1B** (modelo de linguagem para análise e diagnóstico)
- **Biblioteca ollama** (integração Python com o servidor Ollama)
