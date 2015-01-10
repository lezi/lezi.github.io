---
layout: post
draft: false
published: true
date: 2015-01-09 14:58:00
title: Git-Escrevendo mensagens de commit excelentes.
link:
excerpt: As mensagens de commit servem como uma explicação sobre quais alterações foram feitas num determinado commit e as suas motivações. Escrever uma boa mensagem facilita futuras revisões do código e a colaboração com outros desenvolvedores.
category: dev
---

As mensagens de commit servem como uma explicação sobre quais alterações foram feitas num determinado commit e as suas motivações. Escrever uma boa mensagem facilita futuras revisões do código e a colaboração com outros desenvolvedores.

Existem convenções estabelicidas sobre como escrever mensagens de commit idiomáticas e excelentes. Abaixo segue-se um template criado por [Tim Pope](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html):

>Capitalized, short (50 chars or less) summary
>
>More detailed explanatory text, if necessary.  Wrap it to about 72
>characters or so.  In some contexts, the first line is treated as the
>subject of an email and the rest of the text as the body.  The blank
>line separating the summary from the body is critical (unless you omit
>the body entirely); tools like rebase can get confused if you run the
>two together.
>
>Write your commit message in the imperative: "Fix bug" and not "Fixed bug"
>or "Fixes bug."  This convention matches up with commit messages generated
>by commands like git merge and git revert.
>
>Further paragraphs come after blank lines.
>
>- Bullet points are okay, too
>
>- Typically a hyphen or asterisk is used for the bullet, followed by a
>  single space, with blank lines in between, but conventions vary here
>
>- Use a hanging indent
>
>If you use an issue tracker, put references to them at the bottom,
>like this:
>
>Resolves: #123
>
>See also: #456, #789

Este template pode ser resumido em 7 regras simples:

1. Limitar o título a 50 letras
2. Começar o título com maiúsculas
3. Não incluir o ponto no final do título
4. Escrever O título no modo imperativo
5. Separar o título e os parágrafos com uma linha em branco
6. Limitar o corpo da mensagem deve possuir apenas 72 colunas
7. Usar o corpo da mensagem para descrever as alterações respondendo as seguintes perguntas: **O que**, **porquê** e **como**

É fundamental salientar que nem todo commit deverá possuir um título e um corpo. Para alterações simples ao código, uma simples linha pode servir de mensagem de commit, desde que seja claro o suficiente sobre o que foi feito.

## Regras 1, 2 e 3

Apesar de não ser um limite forçado é recomendado que o título ou resumo do commit tenha até 50 caracteres. Este deve representar um sumário conciso das alterações feitas no código.

O título deve começar sempre com letra maiúscula, não conter um ponto no fim.

Exemplo:

><span style="color:green">Alterar o formulário de login</span>

E não:

><span style="color:red">Novo formulário de login.</span>

## Regra 4

Escrever o texto do título de forma imperativa como se fosse um comando.

Evite utilizar títulos como

><span style="color:red">Alterado o formulário de login</span>

><span style="color:red">Novo método para envio de mensagens</span>

## Regras 5 e 6

Separar os parágrafos com uma linha em branco para facilitar a leitura da mensagem.

O texto do corpo da mensagem deve ser restrito a 72 colunas (caracteres e espaços). O git não faz quebra de linha automáticamente. Esta recomendação facilita a leitura do texto num terminal com tamanho normal de 80 colunas. 8 colunas são usadas para indentação à esquerda e à direita e 72 colunas para representar o texto.

## Regra 7

Uma mensagem de commit deve responder às seguintes perguntas:

**O QUE foi feito?**

Descrever de forma clara o que foi feito no commit facilita a rápida identificação das alterações nas futuras revisões do código.

**PORQUÊ foi feito**

Esta questão clarifica as razões que levaram a proceder a determinada alteração no código.

**COMO foi feito**

Deixar claro, em alto nível, as acções realizadas para se efetuar a alteração. Por exemplo

>Remover a duplicação do método `<nome do método>` na classe X

##Conclusão

Estas não são regras obrigatórias. Use algo que se encaixe ao seu projecto e que esteja em concordância com os eventuais colaboradores do código.