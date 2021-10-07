# emojicom

Padrão de mensagem de commit com emojis.

<!-- gist original: https://gist.github.com/nenitf/1cf5182bff009974bf436f978eea1996#emojicom -->

> Adaptação do [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) com emojis do [git3moji](https://robinpokorny.github.io/git3moji/).

## Exemplos

- ``git log``:
  - `:new: allow provided config object to extend other configs`
  - `:100: drop support for Node 6`
  - `:sos: correct spelling of CHANGELOG`
  - `:new:(lang) add polish language`
  - `:bug: correct minor typos in code`
- github:
  - 🆕 allow provided config object to extend other configs
  - 💯 drop support for Node 6
  - 🆘 correct spelling of CHANGELOG
  - 🆕(lang) add polish language
  - 🐛 correct minor typos in code
 
> [Créditos dos commits](https://www.conventionalcommits.org/en/v1.0.0/#examples)

## Motivos

- Poucos tipos de commit para lembrar:
  - 3 para mudanças no produto
  - 3 para mudanças auxiliares
- Estéticamente agradável:
  - Emojis no github
  - Somente 3 letras para todos tipos 👌

## Estrutura

A mensagem de commit deverá seguir a estrutura `<tipo>(<escopo>) <mensagem>`

### `tipo`

**Obrigatório**, tipifica resumidamente a intenção do commit. Devendo ser um dos abaixo (em minúsculo):

- `:bug:` corrige bug inerente ao produto para o cliente final
- `:new:` altera (adiciona, remove, modifica) o produto que o cliente final recebe
- `:100:` altera (adiciona, remove, modifica) o produto que o cliente final recebe, porém não é aparente para o mesmo (refatoração, estilização, comentários etc)
- `:cop:` altera (adiciona, remove, modifica) código de testes
- `:sos:` altera (adiciona, remove, modifica) documentação
- `:zzz:` altera (adiciona, remove, modifica) códigos que ficam ao redor da aplicação, como o processo de build, arquivos de ci e etc

### `escopo`

Opcional, adiciona escopo específico ao tipo. Pode ser usado para descrever modulo entre parênteses que um commit afeta. Exemplo: `:new:(profissionais) adiciona campo de pesquisa de categoria`.
Caso não exista, os parênteses não devem ser usados. Exemplo: `:new: adiciona campo de pesquisa de categoria`.

> Além do escopo opcional, a expressividade do commit pode aumentar com o `!`, especificando quebra de contrato da interface/api (breaking changes) com o usuário final. Deve ser utilizada somente nos commits de `:bug:` e `:new:`. Exemplo: `:new:! muda endpoint /users para /api/users`

### `mensagem`

**Obrigatório**, descreve intenção do commit em uma frase, obedecendo algumas regras:

* Primeira letra minúscula
* Verbo no imperativo (ex: adiciona, remove, modifica, corrige e etc)
* Não deve conter ponto final

## Emojicom x Conventional Commits

```
🐛 :bug: -> fix
🆕 :new: -> feat
💯 :100: -> improve/refactor/style
👮 :cop: -> test
🆘 :sos: -> docs
💤 :zzz: -> chore/build/ci
```

## Shield

[![emojicom](https://img.shields.io/badge/emojicom-%F0%9F%90%9B%20%F0%9F%86%95%20%F0%9F%92%AF%20%F0%9F%91%AE%20%F0%9F%86%98%20%F0%9F%92%A4-%23fff)](http://neni.dev/emojicom)

```md
[![emojicom](https://img.shields.io/badge/emojicom-%F0%9F%90%9B%20%F0%9F%86%95%20%F0%9F%92%AF%20%F0%9F%91%AE%20%F0%9F%86%98%20%F0%9F%92%A4-%23fff)](http://neni.dev/emojicom)
```

## Créditos
- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- [git3moji](https://robinpokorny.github.io/git3moji/)
- [Emoji-Log](https://ahmadawais.com/emoji-log/)
