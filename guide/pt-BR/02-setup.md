# 2. Configure suas ferramentas

Você precisa do Git, de uma conta no GitHub, de uma forma de autenticação, de um editor e das ferramentas necessárias para a linguagem do projeto escolhido. Fazer essa configuração uma vez leva cerca de uma hora.

## Git

Instale o Git:

- **macOS:** `xcode-select --install` (instala o Git com as ferramentas de linha de comando) ou `brew install git` com o [Homebrew](https://brew.sh).
- **Windows:** [Git for Windows](https://git-scm.com/download/win). Ele inclui o Git Bash, um terminal que executa os comandos deste guia.
- **Linux:** use o gerenciador de pacotes da sua distribuição, por exemplo, `sudo apt install git` ou `sudo dnf install git`.

Informe ao Git quem você é. Use o mesmo e-mail da sua conta do GitHub (ou o endereço privado noreply do GitHub, explicado abaixo) para que seus commits sejam associados ao seu perfil:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "voce@example.com"
git config --global init.defaultBranch main
git config --global pull.rebase true
```

### Mantenha seu e-mail privado (opcional)

O GitHub fornece a cada conta um endereço noreply, como `12345678+username@users.noreply.github.com`. Encontre o seu em **Settings → Emails**, ative **Keep my email addresses private** e use esse endereço como `user.email`. Seus commits continuarão aparecendo no seu perfil.

> **Erro comum:** fazer commits com um e-mail que não está associado à sua conta do GitHub. Os commits podem aparecer sem seu avatar e não contar no seu perfil. Confira com `git config user.email` e compare com **Settings → Emails**.

## Uma conta no GitHub e autenticação

1. Crie uma conta em [github.com](https://github.com). Escolha um nome de usuário profissional; ele aparecerá em todas as suas contribuições.
2. Ative a autenticação de dois fatores em **Settings → Password and authentication**. Muitas organizações exigem isso.
3. Configure uma forma de o Git se autenticar. A opção mais simples é a GitHub CLI:

```bash
# macOS: brew install gh   Windows: winget install GitHub.cli   Linux: veja cli.github.com
gh auth login          # escolha GitHub.com, HTTPS e entre pelo navegador
gh auth setup-git      # permite que o Git envie dados por HTTPS usando esse login
```

Como alternativa, [adicione uma chave SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) e clone usando URLs no formato `git@github.com:`.

## Um editor

Use o editor com o qual você se sente confortável. O [VS Code](https://code.visualstudio.com) é uma opção comum: tem boa integração com Git, e as extensões oficiais das linguagens oferecem formatação e verificação de erros. JetBrains IDEs, Neovim, Zed e Emacs também são boas opções.

Duas configurações ajudam a evitar comentários nas revisões:

- **Formatar ao salvar**, usando o formatador do projeto (Prettier, Black, rustfmt, gofmt e outros).
- **Respeitar `.editorconfig`**. Muitos projetos incluem esse arquivo para definir indentação e finais de linha.

## Os comandos Git que você realmente vai usar

| Comando | O que faz |
| --- | --- |
| `git clone URL` | Baixa um repositório |
| `git status` | Mostra o que mudou |
| `git switch -c fix-typo` | Cria e muda para uma nova branch |
| `git add caminho/do/arquivo` | Prepara uma alteração para o próximo commit |
| `git commit -m "mensagem"` | Registra as alterações preparadas |
| `git push -u origin fix-typo` | Envia sua branch |
| `git fetch upstream` | Baixa as alterações mais recentes do projeto original |
| `git rebase upstream/main` | Reaplica seus commits sobre essas alterações |
| `git log --oneline -10` | Mostra os dez commits recentes |
| `git diff` | Mostra alterações ainda não preparadas (`git diff --staged` mostra as preparadas) |

Se você nunca usou Git, passe 30 minutos no [Learn Git Branching](https://learngitbranching.js.org) primeiro. É interativo e cobre exatamente o necessário.

## Ferramentas das linguagens

Instale as ferramentas necessárias para o projeto escolhido, usando a versão solicitada pelo projeto (procure arquivos como `.nvmrc`, `.python-version`, `rust-toolchain.toml`, `go.mod` e `.tool-versions`). Os [guias rápidos por linguagem](../../languages/README.md) listam os comandos mais comuns de cada linguagem.

Gerenciadores de versões tornam isso mais simples:

- **Várias linguagens:** [mise](https://mise.jdx.dev) ou [asdf](https://asdf-vm.com)
- **Node.js:** [fnm](https://github.com/Schniz/fnm) ou nvm, além de `corepack enable` para pnpm e Yarn
- **Python:** [uv](https://docs.astral.sh/uv/) (`uv python install 3.12`)
- **Rust:** [rustup](https://rustup.rs)
- **Go:** o instalador oficial ou o gerenciador de pacotes; o Go baixa ferramentas mais novas automaticamente quando `go.mod` solicita uma versão

## Lista de verificação

- [ ] `git --version` funciona e `git config user.email` corresponde a um e-mail associado à minha conta do GitHub.
- [ ] A autenticação de dois fatores está ativada.
- [ ] `gh auth status` (ou `ssh -T git@github.com`) confirma que consigo me autenticar.
- [ ] Meu editor formata os arquivos ao salvar.

Próximo: [Escolha um projeto](03-choose-a-project.md)
