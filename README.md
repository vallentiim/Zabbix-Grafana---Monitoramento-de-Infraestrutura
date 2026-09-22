# Zabbix + Grafana — Monitoramento de Infraestrutura

Laboratório de monitoramento de infraestrutura desenvolvido com **Zabbix 7 + Grafana**, simulando um ambiente de **NOC (Network Operations Center)** para monitoramento de um computador Windows a partir de um servidor Linux.

O projeto foi desenvolvido como evolução de um laboratório anterior utilizando Zabbix, adicionando o **Grafana** para melhorar a visualização e apresentação das métricas coletadas.

---

##  Objetivo

O objetivo deste projeto é criar um ambiente de monitoramento capaz de:

- Monitorar disponibilidade de hosts;
- Coletar métricas de infraestrutura;
- Monitorar CPU, memória e armazenamento;
- Monitorar serviços do Windows;
- Detectar indisponibilidade de hosts;
- Criar triggers e eventos;
- Visualizar métricas através de dashboards;
- Simular processos utilizados em ambientes NOC;
- Praticar conceitos de monitoramento, observabilidade e infraestrutura.

---

##  Arquitetura

```text
                    ┌─────────────────────────────┐
                    │         Zorin OS 18.1       │
                    │                             │
                    │       Zabbix Server         │
                    │       PostgreSQL            │
                    │       Zabbix Frontend       │
                    │                             │
                    │          Grafana            │
                    └──────────────┬──────────────┘
                                   │
                              Rede Local
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │       Windows Desktop       │
                    │                             │
                    │       Zabbix Agent 2        │
                    │                             │
                    │ CPU | RAM | Disco | Serviços│
                    └─────────────────────────────┘
