# Lista 01 – Flexbox

## Parte A – Múltipla escolha

1. **(b)** No contêiner (pai) cujos filhos se tornarão itens flex.
2. **(c)** `row`
3. **(b)** Horizontal, da esquerda para a direita.
4. **(b)** No eixo vertical (eixo principal).
5. **(c)** `align-items`
6. **(c)** `stretch`
7. **(b)** Coloca o primeiro item no início, o último no fim, e distribui o espaço somente entre eles.
8. **(b)** `wrap`
9. **(b)** O contêiner tem `flex-wrap: wrap` (ou `wrap-reverse`) e mais de uma linha.
10. **(b)** Define o espaço entre os itens, sem criar espaço extra nas bordas externas do contêiner.
11. **(c)** Invertem a ordem visual no eixo horizontal (da direita para a esquerda).
12. **(a)** `justify-content: center;` e `align-items: center;`

## Parte B – Dissertativas e análise de código

### 13.

O contêiner flex é o elemento pai, que recebe `display: flex`. Os itens flex são os filhos diretos dele, que se tornam itens automaticamente e passam a seguir as regras do contêiner.

### 14.

A, B e C ficam empilhados verticalmente, na ordem A, B, C, agrupados no centro vertical do contêiner de 300px. Cada um ocupa toda a largura do contêiner.

### 15.

Os itens passam a ficar lado a lado (`row`). Como o padrão de `flex-wrap` é `nowrap`, não quebram de linha: encolhem até o tamanho mínimo do conteúdo e, se ainda não couberem nos 300px, transbordam o contêiner.

### 16.

(a) Em `row`, `justify-content` atua no eixo horizontal (principal) e `align-items` no vertical (cruzado).

(b) Em `column`, os eixos se invertem: `justify-content` passa a atuar no vertical e `align-items` no horizontal.

### 17.

Porque `align-content` distribui o espaço entre as linhas, e com `nowrap` existe uma só linha. Para ter efeito, é preciso `flex-wrap: wrap`, mais de uma linha e espaço livre no eixo cruzado (por exemplo, com `height` ou `min-height`).

### 18.

O `gap: 16px` cria espaço apenas entre os itens. O `margin-right: 16px` cria espaço também depois do último item, sobrando 16px no final, o que exige exceções como `:last-child { margin-right: 0; }`.

## Parte C – Prática

> Códigos completos em `questao19.html`, `questao20.html`, `questao21.html`, `questao22.html`, `questao23.html` e `questao24.html` (cada um com seu `.css`).

### 19.

```css
.menu {
  display: flex;
  align-items: center;
  gap: 12px;
  margin: 0;
  padding: 0;
  list-style: none;
}
```

### 20.

```css
.galeria {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}
```

### 21.

```css
.pagina {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
```

### 22.

```css
.pagina {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
```

### 23.

```css
.toolbar {
  display: flex;
  justify-content: space-between;
}
```

### 24.

```html
<div class="faixa">
  <div class="card">...</div>
  <div class="card">...</div>
  <div class="card">...</div>
  <div class="card">...</div>
</div>
```

```css
.faixa {
  display: flex;
  flex-wrap: wrap;
  align-items: stretch;
  align-content: flex-start;
  gap: 1rem;
  min-height: 30rem;
}

.card {
  width: 14rem;
  padding: 1rem;
}
```
