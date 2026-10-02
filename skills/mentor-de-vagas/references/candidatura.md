# Preencher candidaturas

## Antes de começar: seja franco sobre o que dá e o que não dá

Preencher formulários exige um navegador controlável **com a sessão da pessoa já logada** (ex.: a extensão Claude in Chrome). Sem isso, você não consegue preencher — nesse caso, entregue um "kit de candidatura" por vaga: link, currículo adaptado, e as respostas prontas para ela copiar e colar.

Explique à pessoa, na primeira vez, a divisão de trabalho:

| Você (Claude) faz | A pessoa faz |
|---|---|
| Abrir a vaga, ler requisitos, apontar alertas | Criar conta e fazer login em cada plataforma (uma vez) |
| Preencher campos de cadastro e de currículo | Digitar senhas, CPF/RG e dados bancários |
| Anexar o currículo adaptado | Resolver CAPTCHA e verificação por e-mail/SMS |
| Responder perguntas factuais com base no perfil | Testes, games, vídeos e avaliações |
| Rascunhar respostas abertas para ela revisar | Aprovar cada envio |

Dica para dar a ela: fazer login antes nas plataformas das vagas escolhidas (LinkedIn, Gupy, Indeed, Eureca, Cia de Talentos…) deixa a sessão muito mais fluida.

## Fluxo, uma vaga por vez

1. **Abra a vaga** e confirme que ainda está aberta. Diga em 1–2 linhas os requisitos-chave e qualquer alerta.
2. **Confira o currículo**: existe versão adaptada em `curriculos/` para esta vaga? Se não, ofereça fazer antes.
3. **Inicie a candidatura.**
   - *Candidatura simplificada (LinkedIn Easy Apply, Indeed)*: avance passo a passo. Para o currículo, anexe o arquivo adaptado; se o upload não for possível no seu ambiente, peça para a pessoa anexar e continue.
   - *Site externo (Gupy, Workday, Greenhouse, Eureca, página própria)*: se pedir login ou cadastro, pare e espere a pessoa. Depois de logada, preencha. Muitas plataformas guardam o perfil — avise quando os dados já estiverem lá e só precisarem de revisão.
4. **Perguntas do formulário:**
   - Fatos presentes em `perfil.md` → responda.
   - "Anos de experiência em X" → conte apenas o que o histórico sustenta; na dúvida, pergunte.
   - Pretensão salarial, disponibilidade, mobilidade, vaga afirmativa/autodeclarações, e tudo que não estiver no perfil → **pergunte à pessoa**, juntando as dúvidas de uma vaga em uma só mensagem. Grave as respostas em `perfil.md` (seção de respostas-padrão) para reutilizar; pretensão salarial, reconfirme a cada vaga, porque costuma variar com o cargo.
   - Perguntas abertas → proponha um rascunho baseado no inventário de conquistas e peça revisão.
   - Aceite de termos, política de privacidade e consentimentos → mostre o que está sendo pedido e deixe a pessoa decidir.
5. **Pare antes do botão final.** Mostre o resumo: vaga, currículo anexado, cada campo e resposta. Pergunte "Posso enviar?". Envie só com um sim explícito para esta vaga.
6. **Confirme o resultado** olhando a tela (mensagem de sucesso, e-mail de confirmação mencionado). Se algo falhar, diga exatamente em que ponto parou — não registre como enviada sem ter visto a confirmação.
7. **Registre** em `vagas.csv`: `enviada`, `pausada` (com o motivo: aguardando login, aguardando teste…) ou `descartada`.

Quando a etapa seguinte for teste, game ou vídeo, pare, explique o que vem pela frente, o prazo, e ofereça ajudar na preparação (tipos de questão, como estruturar um vídeo de apresentação) — sem fazer por ela.

## Fechamento da sessão

Tabela: Empresa · Vaga · Status · Data · Link · Próximo passo.

Se ela quiser, gere uma planilha de acompanhamento a partir de `vagas.csv`. Sugira também o que costuma fazer diferença depois de candidatar: acompanhar o e-mail (inclusive spam), manter o perfil do LinkedIn coerente com o currículo enviado, e preparar-se para a entrevista das vagas mais promissoras — você pode simular a entrevista com ela.
