# 01 - O que é Bootstrap e por que ele existe

[Início](../README.md#roadmap) — [02 - Grid System e Fundamentos »](02-grid-system-fundamentos.md)

---

Imagina montar um guarda-roupa cortando e lixando cada tábua de madeira do zero, toda vez que precisar de um móvel novo. Dá pra fazer? Dá. Vai demorar uma eternidade e provavelmente vai ficar torto? Também. Agora imagina comprar um móvel modular tipo IKEA: as peças já são padronizadas, encaixam entre si, e você só precisa saber montar.

**Bootstrap é o "móvel modular" do desenvolvimento web.** Em vez de escrever CSS do zero pra cada botão, menu e grid de layout, você usa peças prontas, testadas e responsivas — e foca sua energia no que faz seu produto diferente.

## 1.1 – O problema que o Bootstrap resolve

Antes de frameworks CSS existirem (e ainda hoje, quando alguém tenta reinventar a roda), todo projeto novo enfrentava os mesmos problemas:

| Problema | O que acontecia sem framework |
|---|---|
| Layout responsivo | Cada site tinha que calcular do zero como quebrar o layout em celular, tablet e desktop |
| Compatibilidade entre navegadores | Bugs diferentes no Chrome, Firefox e Safari, resolvidos um por um |
| Componentes comuns (botão, menu, modal) | Reescritos do zero em todo projeto, com bugs diferentes toda vez |
| Consistência visual | Cada desenvolvedor do time estilizando do seu jeito, sem padrão |

O Bootstrap nasceu dentro do Twitter, em 2011, exatamente pra resolver isso: um conjunto de CSS e JavaScript prontos, testados por milhões de sites, que resolve os 80% do trabalho repetitivo pra você focar nos 20% que realmente importam pro seu projeto.

> **Curiosidade:** o Bootstrap segue sendo, em 2026, um dos dois frameworks CSS mais usados do mundo (o outro é o Tailwind CSS) — não é uma tecnologia ultrapassada, é só uma ferramenta com um propósito diferente do Tailwind, como vamos ver mais adiante.

## 1.2 – O que é exatamente o Bootstrap?

Bootstrap é um **framework front-end** — um pacote de arquivos CSS e JavaScript que você importa no seu projeto e que já vem com:

- Um **sistema de grid** (grade) para organizar layout em colunas de forma responsiva;
- **Componentes prontos**: botões, cards, formulários, menus de navegação, modais, alertas;
- **Classes utilitárias**: pequenos atalhos de CSS para espaçamento, cor, alinhamento, sem escrever uma linha de CSS customizado;
- Comportamento em **JavaScript** para componentes interativos (dropdown, carrossel, modal), hoje escrito em JavaScript puro, sem depender de jQuery.

## 1.3 – Mobile-First: a mentalidade por trás do Bootstrap

A regra de ouro do Bootstrap (e do design web moderno em geral) é: **projete primeiro para a tela pequena, depois vá escalando para a tela grande.**

Por quê? Porque é mais fácil pegar um layout simples de celular e adicionar espaço e colunas para tela grande do que pegar um layout complexo de desktop e tentar espremer tudo num celular sem quebrar nada.

> **Analogia:** é como fazer as malas para uma viagem. É mais fácil começar com o essencial (a mala pequena) e ir adicionando o que sobrar de espaço, do que fazer a mala enorme primeiro e depois tentar descobrir o que cortar pra caber na mochila.

## 1.4 – Breakpoints: os pontos de quebra do layout

O Bootstrap divide as telas em faixas de tamanho chamadas **breakpoints**. Cada uma tem um prefixo de classe:

| Breakpoint | Prefixo | Largura mínima da tela | Dispositivo típico |
|---|---|---|---|
| Extra small | (nenhum prefixo) | < 576px | Celular na vertical |
| Small | `sm` | ≥ 576px | Celular na horizontal |
| Medium | `md` | ≥ 768px | Tablet |
| Large | `lg` | ≥ 992px | Notebook |
| Extra large | `xl` | ≥ 1200px | Desktop |
| Extra extra large | `xxl` | ≥ 1400px | Monitor grande |

Isso vai fazer muito mais sentido no Módulo 2, quando falarmos do Grid System — mas grava esse conceito, porque ele aparece em praticamente toda classe do Bootstrap (`col-md-6`, `d-lg-flex`, etc.).

## 1.5 – Seu primeiro Hello World com Bootstrap

O jeito mais rápido de começar (sem instalar nada) é usar o Bootstrap via CDN. Crie um arquivo `index.html` com este conteúdo:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Primeiros passos com Bootstrap</title>
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css"
    rel="stylesheet">
</head>
<body>

  <div class="container mt-5">
    <h1 class="text-primary">Oi, mundo Bootstrap!</h1>
    <p class="lead">Isso aqui já está estilizado sem eu escrever uma linha de CSS.</p>
    <button type="button" class="btn btn-success">Meu primeiro botão</button>
  </div>

  <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js">
  </script>
</body>
</html>
```

Abra esse arquivo no navegador. Repare: você não escreveu **nenhum** CSS customizado e já tem uma fonte legível, espaçamento decente, cor de texto e um botão estilizado. Isso é o Bootstrap fazendo o trabalho pesado.

## 1.6 – Bootstrap x Tailwind x CSS puro: qual escolher?

Essa pergunta é feita toda semana em fóruns de desenvolvimento, então vamos analisar de forma objetiva:

| Critério | Bootstrap | Tailwind CSS | CSS puro |
|---|---|---|---|
| Filosofia | Componentes prontos (botão, card, navbar já estilizados) | Classes utilitárias (você monta o visual combinando classes pequenas) | Você escreve tudo |
| Velocidade para prototipar | Muito rápida | Rápida, mas com curva de aprendizado | Lenta |
| Visual pronto | Sim, precisa customizar para fugir do padrão | Não, o visual final é totalmente seu | Não, é 100% seu |
| Cenário ideal | Protótipos rápidos, dashboards internos, MVPs, quem não tem designer dedicado | Produtos com identidade visual forte e time de design definido | Aprender fundamentos ou projetos com necessidade visual muito específica |

> **Nota:** Nenhum dos três é melhor de forma absoluta — são ferramentas diferentes para contextos diferentes. Quem diz que Bootstrap "morreu" geralmente só prefere outra ferramenta. Este guia foca em Bootstrap porque, para quem está começando, é o caminho mais direto do zero a uma tela funcional e responsiva.

## 1.7 – Mão na massa

Antes de seguir para o Módulo 2:

- [ ] Crie o arquivo `index.html` da seção 1.5 e abra no navegador;
- [ ] Troque `btn-success` por `btn-danger`, `btn-warning` e `btn-info` — veja o que muda;
- [ ] Redimensione a janela do navegador (ou abra o DevTools em modo responsivo) e observe o que acontece com o texto e o espaçamento;
- [ ] Escreva, com suas próprias palavras, o que significa "mobile-first" para alguém que nunca ouviu o termo.

## 1.8 – Checklist de saída do módulo

Você está pronto para o Módulo 2 se consegue responder, sem colar:

- [ ] Por que frameworks CSS existem e qual problema eles resolvem;
- [ ] O que significa "mobile-first" e por que essa ordem importa;
- [ ] Os nomes e a ordem dos breakpoints do Bootstrap (sm, md, lg, xl, xxl);
- [ ] A diferença de filosofia entre Bootstrap e Tailwind CSS.

---

Termos novos? Consulte o [Glossário](glossario.md) ou veja as [Ferramentas Recomendadas](ferramentas-recomendadas.md).

---

<div align="center">
  <a href="../README.md#roadmap">Índice</a> — <a href="02-grid-system-fundamentos.md">02 - Grid System e Fundamentos »</a>
</div>
