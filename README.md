# Mentor de Vagas

Uma skill para o [Claude](https://claude.ai) que funciona como mentor de carreira e assistente de busca de emprego, pensada para o mercado brasileiro. Serve para qualquer pessoa e qualquer área.

## O que ela faz

1. **Lê seu currículo** e dá um diagnóstico franco: pontos fortes e o que está enfraquecendo.
2. **Faz uma mentoria de RH** — uma conversa para descobrir resultados e habilidades que você tem e não colocou no papel.
3. **Aconselha sobre que vagas buscar**, incluindo cargos vizinhos que você talvez não tenha considerado.
4. **Procura vagas** em LinkedIn, Gupy, Indeed, Vagas.com, programas de trainee e páginas de carreira, e entrega uma lista ranqueada com os alertas de cada vaga.
5. **Gera um currículo adaptado para cada vaga**, em formato que os sistemas de triagem (ATS) leem bem — sem inventar nada.
6. **Ajuda a preencher as candidaturas** e só envia quando você confirma.
7. **Busca diária**: pode rodar todo dia e mostrar só as vagas novas.

## O que ela não faz (de propósito)

- Não cria contas nem digita senhas — login e cadastro em cada site são com você (normalmente uma vez por plataforma).
- Não resolve CAPTCHA, não faz testes, games ou vídeos por você.
- Não envia candidatura sem o seu "sim".
- Não inventa experiência, curso ou nível de idioma.

## Do que você precisa

- Aplicativo **Claude para desktop** (plano pago, com skills habilitadas).
- Para preencher candidaturas: a extensão **Claude in Chrome** instalada e conectada, com você logada nos sites de vagas.
- Para a busca diária: criar uma tarefa agendada no aplicativo (a skill orienta), com o computador ligado e o app aberto no horário.

Sem a extensão do Chrome a skill ainda funciona para mentoria, busca e currículos; só o preenchimento automático fica de fora.

## Instalação

### Opção A — arquivo .zip (mais simples)

1. Baixe `mentor-de-vagas.zip` na página de [Releases](../../releases) deste repositório.
2. No aplicativo Claude: **Configurações → Recursos (Capabilities) → Skills → Enviar skill**.
3. Selecione o arquivo e ative a skill.

### Opção B — como plugin (Claude Code / aba Code do aplicativo)

```
/plugin marketplace add vitorsantos-ia/mentor-de-vagas
/plugin install mentor-de-vagas@mentor-de-vagas
```

## Como usar

Escolha uma pasta no seu computador para a skill guardar seus dados (ex.: `Documentos/Minhas Vagas`), abra o Claude nessa pasta e diga algo como:

> Quero ajuda para procurar emprego. Segue meu currículo. Procuro vagas de analista de marketing em São Paulo.

Nas próximas vezes, basta abrir na mesma pasta e dizer **"vagas de hoje"** ou **"quero me candidatar às vagas 2 e 5"**.

## Privacidade

Seus dados ficam em arquivos na **sua** pasta (`perfil.md`, `vagas.csv`, `curriculos/`). Nada pessoal faz parte deste repositório. Se você fizer um fork e usar a própria pasta do repositório para trabalhar, o `.gitignore` já impede que esses arquivos sejam enviados.

## Aviso

Automatizar ações em sites de vagas pode contrariar os termos de uso de algumas plataformas (como o LinkedIn). A skill trabalha em ritmo humano, com volume baixo e aprovação sua a cada envio, justamente para reduzir esse risco — mas o uso é por sua conta.

## Estrutura

```
skills/mentor-de-vagas/
├── SKILL.md                  fluxo geral e regras
├── references/
│   ├── mentoria.md           entrevista de RH e direcionamento de vagas
│   ├── busca.md              fontes, filtros e ranqueamento
│   ├── curriculo-ats.md      adaptação e formato ATS
│   ├── candidatura.md        preenchimento de formulários
│   └── rotina-diaria.md      busca agendada
└── assets/
    └── perfil-modelo.md      modelo do arquivo de perfil
```

## Licença

MIT
