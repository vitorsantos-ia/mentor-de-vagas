# Rotina diária de vagas

Uma skill não roda sozinha: quem dispara a busca todo dia é uma **tarefa agendada** do aplicativo. Esta etapa configura essa tarefa e define como ela se comporta.

## Configurar (com a pessoa presente)

Ofereça a rotina depois da primeira busca bem-sucedida, quando `perfil.md` já tem cargos-alvo definidos.

1. Combine o horário e os dias (padrão: dias úteis, de manhã).
2. Verifique se há uma ferramenta de agendamento disponível (tarefas agendadas / scheduled tasks).
   - **Há** → crie a tarefa com o texto abaixo, ajustando o caminho da pasta.
   - **Não há** → explique que, no aplicativo Claude para desktop, ela pode criar a tarefa na área de tarefas agendadas e colar o mesmo texto. Como alternativa simples: abrir o Claude e dizer "vagas de hoje".
3. Explique as condições: o computador precisa estar ligado e o aplicativo aberto no horário; o resultado aparece como uma nova conversa no Claude.

Texto da tarefa:

```
Use a skill mentor-de-vagas no modo "rotina diária".
Pasta da pessoa: <CAMINHO DA PASTA COM perfil.md>
Busque vagas publicadas nas últimas 48 horas para os cargos-alvo do perfil,
ignore as que já estão em vagas.csv e me mostre apenas as novas.
Não preencha nem envie nenhuma candidatura.
```

## Como se comportar no modo rotina diária

A pessoa não está presente durante a execução, então:

- **Só busca e relatório.** Nenhuma candidatura, nenhum formulário, nenhum currículo novo. Tudo isso espera a pessoa escolher.
- **Não faça perguntas** no meio — use os defaults do perfil. Dúvidas vão para o fim do relatório.
- Leia `perfil.md` e `vagas.csv`; siga `references/busca.md` com janela de 24–48 h e no máximo 2 páginas por termo. Se o navegador logado não estiver disponível, use busca na web e diga isso no relatório.
- Inclua vagas com prazo fechando nos próximos dias que já estavam em `vagas.csv` como `escolhida` ou `cv-pronto` mas ainda não foram `enviada` — é o lembrete mais útil que a rotina pode dar.

## Formato do relatório

Curto, para ser lido em um minuto:

```
Vagas de <data> — <N> novas

[tabela no formato de references/busca.md, só com as novas, no máximo 8]

Links
1. ...

⏰ Prazos chegando: <vagas escolhidas ainda não enviadas, com data>
Ficou de fora: <resumo em uma linha>
Fontes que não consegui ler hoje: <se houver>

Quais números você quer que eu prepare o currículo e a candidatura?
```

Dia sem vagas boas: diga isso em uma linha, sem forçar lista. Se forem vários dias seguidos sem nada, sugira ampliar (cargos vizinhos, outras cidades, remoto) na próxima conversa.

Grave as novas em `vagas.csv` com status `nova`.
