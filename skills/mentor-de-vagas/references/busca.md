# Busca, filtro e ranqueamento de vagas

## Preparação

De `perfil.md`, pegue: cargos-alvo e seus termos, cidades, modelo de trabalho, nível, inegociáveis. Defaults quando não houver informação:

- Janela: últimos 14 dias na primeira busca; últimas 24–48 h na rotina diária.
- Nível: o compatível com a experiência comprovada — descarte o que está claramente abaixo ou acima.
- Para cada cargo-alvo, 2 a 4 variações de termo (sinônimos, PT/EN, com e sem nível).

Leia `vagas.csv` antes de começar, para não repetir o que já foi mostrado.

## Ferramentas, em ordem de preferência

1. **Navegador com a sessão logada da pessoa** (ex.: Claude in Chrome). Dá os melhores resultados e é o único caminho que depois permite preencher candidaturas. Se as ferramentas de navegador precisarem ser carregadas, carregue todas de uma vez.
2. **Busca na web e leitura de páginas públicas** (WebSearch / WebFetch ou equivalente). Funciona sem login, com cobertura menor.
3. **Nenhuma das duas** → diga isso claramente e ofereça o que dá: montar os links de busca prontos para a pessoa abrir, e analisar vagas que ela colar na conversa.

Se um site pedir login, peça para a pessoa logar e aguarde. Nenhuma plataforma cobre tudo e algumas (Indeed, Glassdoor) bloqueiam leitura automatizada com frequência; quando uma fonte falhar, diga qual falhou em vez de fingir cobertura completa.

## Onde procurar

**LinkedIn** — principal fonte para vagas corporativas.
```
https://www.linkedin.com/jobs/search/?keywords=<TERMO>&location=<LOCAL>&f_TPR=r1209600&sortBy=DD
```
- `f_TPR`: `r86400` 24 h · `r604800` 7 dias · `r1209600` 14 dias · `r2592000` 30 dias
- `f_E` (nível): `1` estágio · `2` júnior · `3` assistente/associate · `4` pleno-sênior · `5` diretoria (combine com `%2C`). O filtro é impreciso: confira título e descrição.
- `f_WT` (modelo): `1` presencial · `2` remoto · `3` híbrido
- `f_AL=true` só candidatura simplificada — não use por padrão; exclui muitas empresas grandes que recebem candidatura em site próprio.
- Paginação: `start=0,25,50`. No máximo 3 páginas por termo.

**Gupy** — muitas empresas grandes no Brasil publicam aqui primeiro.
```
https://portal.gupy.io/job-search/term=<TERMO>
```

**Outras fontes, conforme o perfil:**
- Geral: Indeed (`br.indeed.com/jobs?q=<TERMO>&l=<CIDADE>`), Vagas.com, Catho, InfoJobs, Glassdoor.
- Trainee e estágio: Cia de Talentos, Eureca, 99jobs, Across, Matchbox, CIEE, Nube, e as páginas de carreira das empresas. Programas de trainee costumam ser nacionais, abrir entre agosto e novembro e ter prazo curto — busque por "programa de trainee <ano seguinte> inscrições abertas" + área, e sempre capture o **prazo de inscrição**.
- Tecnologia/startups: Programathor, GeekHunter, Remotar, páginas Greenhouse/Lever/Workable das empresas.
- Empresas-alvo: se a pessoa citou empresas dos sonhos, visite a página de carreiras de cada uma.
- Busca aberta: `"<cargo>" "<cidade>" vaga` e `site:<plataforma> "<cargo>" "<cidade>"`.

## O que capturar de cada vaga

Título · empresa · cidade e modelo · data de publicação · plataforma e tipo de candidatura (simplificada ou site externo) · link direto · prazo, se houver · principais requisitos · salário, se informado.

Abra a descrição completa pelo menos das vagas que vão para a lista final — título sozinho engana.

## Filtrar

Descarte, anotando o motivo para o resumo final:

- Nível fora do perfil; cidade/modelo que contraria um inegociável.
- Duplicadas (a mesma vaga em duas plataformas ou repostada) — fique com o link de candidatura mais direto.
- Já presentes em `vagas.csv`.
- Prazo encerrado.
- Sinais de golpe (ver regras gerais na SKILL.md).
- "Empresa confidencial" e recrutadoras genéricas vão para o fim da fila, salvo se a descrição for claramente boa.

## Ranquear

Dê duas notas de 0 a 5 e seja capaz de justificar cada uma em uma frase:

- **Aderência** — quanto as habilidades *comprovadas* em `perfil.md` cobrem os requisitos da vaga. Requisito obrigatório que a pessoa não tem derruba a nota.
- **Empresa** — porte, reputação e solidez, segundo o que a pessoa valoriza (alguns querem multinacional, outros startup, outros estabilidade). Na dúvida sobre uma empresa, pesquise rapidamente; não suponha.

Ajustes: +1 publicada há ≤ 7 dias · +0,5 candidatura simplificada · −1 com muitos candidatos (>200) · prazo fechando em ≤ 7 dias ganha destaque.

`Score = Aderência × 0,5 + Empresa × 0,4 + ajustes`. Aderência pesa mais porque uma vaga excelente para a qual a pessoa não passa na triagem só gasta a energia dela.

## Apresentar

De 8 a 12 vagas (menos se não houver boas — lista curta e honesta vale mais que lista cheia).

| # | Empresa | Vaga | Local / modelo | Publicada | Candidatura | Por que faz sentido | Atenção |
|---|---|---|---|---|---|---|---|
| 1 | Exemplo S.A. | Analista de Marketing Pleno | São Paulo · híbrido | há 3 dias | Gupy | Eventos e materiais de venda, como no seu último cargo | Pede inglês avançado |

- **Atenção** traz o gap real entre a vaga e o perfil, ou "—". É a coluna que mais ajuda a pessoa a decidir; não suavize.
- Links numerados logo abaixo da tabela (`1. <url>`).
- Programas de trainee em tabela separada (T1, T2…), com colunas: Empresa · Programa/trilha · Inscrições até · Requisitos-chave · Plataforma · Atenção — ordenada pelo prazo mais próximo.
- Uma linha final com o que ficou de fora e por quê, e quais fontes não puderam ser lidas.

Grave todas as vagas mostradas em `vagas.csv` com status `nova`.

Termine perguntando quais números ela quer levar adiante e pare. Quando ela responder, marque as escolhidas como `escolhida` e as rejeitadas como `descartada` — e, se ela disser por que rejeitou, guarde isso em `perfil.md` como preferência, para afinar as próximas buscas.
