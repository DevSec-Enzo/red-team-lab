# 🔴 red-team-lab

Documentação técnica de labs e desafios de segurança ofensiva, resolvidos
na plataforma [TryHackMe](https://tryhackme.com/).

## Sobre

Este repositório reúne meus writeups de Red Team / Pentest — minha área de
especialização de carreira em cibersegurança. Cada entrada documenta o
processo completo: reconhecimento, enumeração, exploração e análise de
impacto da vulnerabilidade encontrada.

## Salas documentadas

| Sala | Categoria | Nível | Writeup |
|---|---|---|---|
| Offensive Security Intro | Fundamentos | Easy | [Ver writeup](./tryhackme/offensive-security-intro) |
| CyberHeroes | Web / Authentication | Easy | [Ver writeup](./tryhackme/tryhackme-challenges-writeups/cyberheroes) |

## Estrutura

```
red-team-lab/
└── tryhackme/
    ├── offensive-security-intro/
    │   ├── README.md
    │   └── screenshots/
    └── tryhackme-challenges-writeups/
        └── cyberheroes/
            ├── README.md
            └── screenshots/
```

## Metodologia

Todo writeup segue o mesmo formato:

1. **Reconhecimento** — mapeamento inicial da aplicação/alvo
2. **Enumeração** — inspeção de código-fonte, requisições e respostas HTTP
3. **Exploração** — passo a passo até a obtenção de acesso/flag
4. **Impacto** — explicação técnica da causa raiz da vulnerabilidade

Dados sensíveis (IPs, credenciais, flags) são ocultados nos prints, conforme
as diretrizes das plataformas utilizadas.

## Contato

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/enzo-almeida-sec/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/DevSec-Enzo)