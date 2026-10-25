# 3. Escolha um projeto

O projeto importa mais do que a issue. Um projeto ativo e acolhedor pode revisar seu pull request em poucos dias. Um projeto inativo ou sobrecarregado talvez nunca o analise, por melhor que seja sua contribuição.

## Comece pelo que você usa

O melhor primeiro projeto é um que você já usa: uma biblioteca presente no seu próprio código, uma ferramenta que você executa todos os dias ou um aplicativo de que gosta. Você entende como ele deveria funcionar, consegue testar sua alteração na prática e se importa com o resultado.

Se nenhum projeto vier à mente, navegue pelo [índice de issues](../../issues/README.md), filtrando pela linguagem que você conhece melhor, e observe quais projetos aparecem com frequência.

## Sinais de um projeto saudável e acolhedor

Confira estes pontos na página do repositório. Cinco minutos aqui podem poupar semanas de espera.

| Verificação | Onde procurar | Bom sinal |
| --- | --- | --- |
| Atividade recente | Aba Commits, data do último commit | Houve commits nas últimas semanas |
| Contribuições externas mescladas | **Pull requests → Closed**, filtre por `is:merged` e veja os autores | Pull requests de pessoas que não são mantenedoras foram mesclados no último mês |
| Velocidade das revisões | Abra alguns PRs recentes de pessoas externas que foram mesclados | A primeira resposta chega em dias, não meses |
| Guia de contribuição | `CONTRIBUTING.md` na raiz, `.github/` ou `docs/` | Existe e explica a configuração e os testes |
| Etiquetas para iniciantes | Issues, filtre por `good first issue` ou `help wanted` | As etiquetas são usadas e as issues marcadas recebem atenção |
| Tom das conversas | Leia algumas discussões de issues | Mantenedores são pacientes e específicos, mesmo quando recusam algo |
| Código de conduta | `CODE_OF_CONDUCT.md` | Existe |
| Integração contínua (CI) | Verificações em PRs recentes | Os testes são executados automaticamente nos pull requests |

Uma busca rápida mostra PRs mesclados de colaboradores externos em qualquer repositório (substitua `OWNER/REPO`):

```text
https://github.com/OWNER/REPO/pulls?q=is:pr+is:merged+-author:app/dependabot+sort:updated-desc
```

Observe os autores: se todos os PRs mesclados vierem das mesmas duas pessoas, talvez as contribuições externas não sejam prioridade nesse projeto.

## Sinais de alerta

- **Centenas de pull requests abertos sem revisão.** O seu entrará na fila.
- **Um guia de contribuição que diz que o projeto não está aceitando pull requests**, ou que só aceita contribuições para issues com uma etiqueta específica. Alguns projetos populares funcionam assim. Respeite essa regra.
- **Várias propostas de PR para cada issue recente.** Projetos populares podem receber PRs de pessoas que chegam de passagem poucas horas depois de um bug ser relatado. Ainda é possível contribuir, mas prefira tarefas menos disputadas (documentação, testes ou bugs antigos confirmados) ou um projeto menor.
- **Mantenedores pedindo que as pessoas parem de abrir pull requests de pouco esforço.** Leia essas conversas: elas explicam exatamente o que evitar.
- **Nenhum commit há meses.** O projeto pode estar concluído ou abandonado.

## Projeto grande ou pequeno?

| | Projeto grande e famoso | Projeto menor e ativo |
| --- | --- | --- |
| Concorrência por issues fáceis | Muito alta | Baixa |
| Velocidade da revisão | Varia bastante; costuma ser lenta para pessoas externas | Muitas vezes rápida e direta |
| Processo | Formal: modelos, CLAs e CI rigorosa | Mais simples |
| Mentoria | Às vezes há programas estruturados | Contato direto com o mantenedor |
| Destaque no perfil | Reconhecimento pelo nome conhecido | Forte se você se tornar colaborador frequente |

Uma boa estratégia: faça suas primeiras uma ou duas contribuições em um projeto menor e ativo, onde possa receber feedback rapidamente, e depois aplique o que aprendeu em projetos maiores.

## Lista de verificação

- [ ] O projeto teve commits no último mês.
- [ ] Mesclou recentemente pull requests de colaboradores externos.
- [ ] Tem um guia de contribuição, e eu o li.
- [ ] Consigo compilar e executar o projeto na minha máquina (o capítulo 5 aborda isso).

Próximo: [Encontre uma issue que você consiga concluir](04-find-an-issue.md)
