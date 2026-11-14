# Hábitos

App web (PWA) para registrar, acompanhar e analisar hábitos. Funciona no celular e no PC, com dados sincronizados pelo Firebase.

## Funcionalidades
- **Hoje:** check, quantidade (ml, páginas, minutos) ou horário; alerta de "não falhar 2x"; humor e anotações do dia.
- **Hábitos:** tudo editável — área, prioridade (Inegociável / Não falhar 2x), frequência (diária, dias específicos ou X vezes por semana), meta por dia da semana, passo a passo e lembrete. Mudanças valem a partir do dia em que são feitas, sem alterar o histórico.
- **Metas:** da semana, do mês e do ano, com status, prazo e progresso numérico.
- **Análises:** % por dia, semana, mês e ano; por área; ranking; dia da semana; sequências; humor × hábitos; calendário do ano.

## Estrutura
| Arquivo | Para quê |
|---|---|
| `index.html` | O app inteiro (HTML, CSS e JS) |
| `firebase-config.js` | Configuração pública do app web no Firebase |
| `firestore.rules` | Regras de segurança do Firestore (cada usuário só acessa os próprios dados) |
| `manifest.webmanifest`, `sw.js`, `icons/` | Instalação como app (PWA) e funcionamento offline |

## Dados no Firestore
```
users/{uid}/docs/meta        → hábitos, metas, áreas e configurações
users/{uid}/docs/m-AAAA-MM   → checks e diário de cada mês
```

## Publicação
Hospedado no GitHub Pages a partir da branch `main`. Qualquer push na `main` atualiza o app.
