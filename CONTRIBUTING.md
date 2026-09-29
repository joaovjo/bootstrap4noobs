# Como Contribuir com o Bootstrap4Noobs

Ficamos muito felizes pelo seu interesse em colaborar! O **Bootstrap4Noobs** é um projeto comunitário, gratuito e aberto. Toda ajuda é bem-vinda: desde consertar um link quebrado ou corrigir uma classe do Bootstrap, até escrever um capítulo inteiro ou criar um exemplo de layout.

---

## Antes de começar

- **Mudanças pequenas (typos, links, correções pontuais):** pode abrir o Pull Request direto.
- **Mudanças grandes (novo módulo, reestruturação de conteúdo ou exemplos complexos):** abra uma issue primeiro para alinharmos a ideia antes de você gastar horas escrevendo código.

---

## Passo a passo no Git

1. Faça um **fork** deste repositório para o seu perfil no GitHub.
2. Clone o seu fork na sua máquina:
   ```bash
   git clone https://github.com/SEU-USUARIO/bootstrap4noobs.git
   cd bootstrap4noobs
   ```
3. Crie uma branch com um nome que descreva o que você vai fazer:
   ```bash
   git checkout -b feat/exemplo-navbar
   # ou para correções:
   git checkout -b fix/typo-grid
   ```
4. Faça suas edições seguindo o nosso [padrão de escrita](#padrão-de-escrita) e de código.
5. Verifique suas alterações:
   ```bash
   git status
   git diff
   ```
6. Crie commits semânticos e claros:
   ```bash
   git commit -m "docs: adiciona exemplos práticos de cards no modulo 3"
   ```
7. Envie a branch para o seu fork:
   ```bash
   git push origin feat/exemplo-navbar
   ```
8. Abra o **Pull Request** no GitHub detalhando o que foi feito com base no template que vai aparecer na tela.

---

## Padrão de escrita

Para manter o guia agradável e consistente para quem está lendo, seguimos estes princípios:

1. **Foco no iniciante absoluto:** Nunca assuma que a pessoa já sabe conceitos intermediários. Se usar um termo técnico como *breakpoint*, *viewport* ou *gutters*, explique brevemente o que significa antes de seguir.
2. **Mostre o código em ação:** Evite teoria abstrata sem exemplo. Mostre a marcação HTML real e como as classes do Bootstrap afetam o visual.
3. **Tom de dev real:** Escreva como se estivesse explicando algo para um colega ao lado no café. Sem linguagem empolada, sem jargões corporativos e sem clichês vazios gerados por IA (nada de "vamos mergulhar", "revolucionário" ou "sem mais delongas").
4. **Alinhamento com a documentação oficial:** A base é a versão estável do Bootstrap 5 (https://getbootstrap.com/docs/5.3/). Não utilize classes obsoletas do Bootstrap 4 (como `form-row` ou `float-left`).

---

## Estrutura de um módulo

Todo módulo dentro da pasta `modulos/` fica em seu próprio diretório no formato `NN-nome-do-modulo/README.md` e deve seguir este esqueleto:

````markdown
# Módulo NN: Título do Módulo 📐

[⬅️ Módulo Anterior](../NN-anterior/README.md) | [🏠 Início](../../README.md) | Próximo: [Módulo Seguinte →](../NN-proximo/README.md)

---

Parágrafo curto explicando a dor real: qual problema este recurso resolve e por que ele existe.

## 1. Conceito na prática

Explicação direta acompanhada de analogia simples quando couber.

```html
<!-- Exemplo mínimo funcional -->
<div class="container text-center">
  <div class="row">
    <div class="col">Coluna 1</div>
    <div class="col">Coluna 2</div>
  </div>
</div>
```

## 2. Erros comuns de quem está começando

O que a maioria das pessoas erra ao usar esse recurso (exemplo: esquecer a `row` antes de declarar a `col`).

## 3. Exercício rápido

Uma pequena tarefa prática para quem está lendo testar no navegador.

---

<div align="center">
  <a href="../NN-anterior/README.md">« Módulo Anterior</a> — <a href="../../README.md#roadmap">Índice</a> — <a href="../NN-proximo/README.md">Próximo Módulo »</a>
</div>
````

---

## Onde tirar dúvidas?

Temos um canal exclusivo para o projeto e outros guias da comunidade:
Acesse o **Discord da HE4RT Developers**: https://discord.gg/he4rt e procure o canal `#4noobs`.

Obrigado por ajudar a tornar a comunidade dev mais forte! 💜
