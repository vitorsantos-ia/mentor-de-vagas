# Currículo adaptado por vaga, em formato ATS

ATS (Applicant Tracking System) é o sistema que as empresas usam para receber e triar currículos — Gupy, Workday, Greenhouse, Kenoby e outros. Ele extrai o texto do arquivo e compara com os requisitos da vaga. Um currículo bonito que o sistema não consegue ler, ou que não usa as palavras da vaga, é descartado antes de um humano ver.

## Passo 1 — Ler a vaga como um recrutador

Da descrição completa, extraia:

- **Requisitos obrigatórios** e **desejáveis**.
- **Palavras-chave**: nomes de ferramentas, metodologias, tipos de atividade, termos do setor — na grafia exata que a vaga usa.
- **O problema que a vaga resolve**: o que essa pessoa vai entregar nos primeiros meses.

Cruze com `perfil.md` e classifique cada requisito: ✅ comprovado · 🟡 parcial/transferível · ❌ não tem. Mostre esse quadro à pessoa em poucas linhas antes de escrever. Se faltar um obrigatório importante, diga — às vezes vale candidatar mesmo assim, às vezes não, e a decisão é dela.

## Passo 2 — Adaptar sem inventar

O que muda de uma versão para outra:

- **Título/objetivo** alinhado ao nome da vaga (quando verdadeiro para o perfil).
- **Resumo profissional** (3–4 linhas) reescrito para responder ao problema da vaga.
- **Ordem e seleção dos bullets** em cada experiência: os mais relevantes para esta vaga sobem; os irrelevantes encolhem ou saem.
- **Vocabulário**: se a pessoa fez a coisa, use o termo que a vaga usa para ela (ela escreveu "ações em loja", a vaga diz "ativações de PDV" — use o da vaga).
- **Competências**: as que a vaga pede e a pessoa tem, primeiro.

O que não muda: fatos. Cargos, empresas, datas, formação, nível de idioma e números permanecem os de `perfil.md`. Requisito ❌ não entra no currículo. Requisito 🟡 entra descrito como realmente é ("conhecimento básico em Power BI"), nunca promovido.

Encher o currículo de palavras-chave soltas ou esconder texto em branco não funciona: os sistemas atuais detectam e o recrutador humano lê em seguida.

## Passo 3 — Estrutura que ATS lê bem

- **Uma coluna**, de cima para baixo. Sem tabelas, caixas de texto, colunas, ícones, foto, gráficos de "nível de habilidade".
- Nada de informação importante em cabeçalho/rodapé do arquivo — muitos sistemas ignoram.
- Fonte comum (Arial, Calibri), 10,5–12 pt, bullets simples.
- **Títulos de seção padrão**, nesta ordem:
  1. Nome e contato (cidade/UF, telefone, e-mail, LinkedIn) — no corpo do documento
  2. Objetivo (o título da vaga)
  3. Resumo profissional
  4. Experiência profissional — `Cargo | Empresa | Cidade | mm/aaaa – mm/aaaa`, ordem do mais recente para o mais antigo
  5. Formação acadêmica
  6. Idiomas
  7. Competências e ferramentas
  8. Cursos e certificações / Projetos (se relevantes)
- **Bullets**: verbo de ação + o que fez + resultado ou escala. 3 a 6 por experiência recente, menos nas antigas.
- **Tamanho**: 1 página até ~8 anos de experiência; 2 no máximo.
- No Brasil não se coloca CPF, RG, estado civil, foto nem endereço completo.
- Datas sempre no mesmo formato. Siglas com o termo por extenso na primeira vez.
- Vaga em inglês → currículo em inglês; caso contrário, português.

## Passo 4 — Gerar o arquivo

- Formato: **.docx** (é o que os sistemas leem com mais segurança) e, se a pessoa quiser, também PDF de texto — nunca PDF de imagem/escaneado.
- Se houver uma skill de criação de documentos Word disponível (ex.: `docx`), use-a. Sem ferramenta para gerar arquivo, entregue o texto pronto para colar em um modelo simples.
- Salve em `curriculos/` com nome claro: `CV - <Nome> - <Empresa> - <Vaga>.docx`. O nome do arquivo aparece para o recrutador.
- Não sobrescreva o currículo base.

## Passo 5 — Mostrar e confirmar

Apresente à pessoa:

- As 3–5 mudanças principais em relação ao currículo base e o motivo de cada uma.
- Os requisitos da vaga que continuam sem cobertura.
- Qualquer frase em que você tenha dúvida se representa fielmente o que ela fez — pergunte.

Só depois da aprovação dela, atualize `vagas.csv` para `cv-pronto` e ofereça seguir para a candidatura.

Quando a vaga pedir carta de apresentação ou tiver pergunta aberta ("por que você quer trabalhar aqui?"), ofereça um rascunho curto baseado no inventário de conquistas, para ela revisar e deixar com a voz dela.
