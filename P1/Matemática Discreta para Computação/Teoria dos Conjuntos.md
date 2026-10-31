# Teoria dos Conjuntos

## O que é um conjunto?

Um conjunto é uma coleção de elementos. É um dos conceitos mais fundamentais da matemática e o objeto central da teoria dos conjuntos.

A relação entre um objeto e um conjunto é a de pertinência: se x é um dos elementos de A, dizemos que x pertence a A.

**Exemplos**
- Uma coleção de números é um conjunto, {2, 4, 6}.
- Uma coleção de vogais é um conjunto, {𝑎, 𝑒, 𝑖, 𝑜, 𝑢}.
- Uma coleção de cores é um conjunto, {𝑣𝑒𝑟𝑑𝑒, 𝑎𝑧𝑢𝑙, 𝑣𝑒𝑟𝑚𝑒𝑙ℎ𝑜}.

## Notação

Há três formas de descrever um conjunto:

1. **Extensão:** listar todos os seus elementos.
2. **Compreensão:** enunciar uma propriedade que seus elementos satisfazem (isso exige cuidado, pois uma definição descuidada pode gerar paradoxos).
3. **Representação gráfica:** usar Diagramas de Venn.

## Conjuntos Especiais

- **Conjunto universo (U):** contém todos os elementos considerados em uma dada situação; todos os conjuntos em questão são seus subconjuntos.
- **Conjunto vazio ({ } ou ∅):** o único conjunto sem elementos, com cardinalidade zero.

### Conjuntos numéricos

- **Naturais (ℕ):** números de contagem, ℕ = {0, 1, 2, 3, ...}. O zero é incluído por ter as mesmas propriedades algébricas.
- **Inteiros (ℤ):** naturais e seus simétricos negativos, ℤ = {..., −2, −1, 0, 1, 2, ...}.
- **Racionais (ℚ):** números que podem ser escritos como fração m/n, com m, n ∈ ℤ e n ≠ 0, ℚ = {x | x = m/n, m, n ∈ ℤ, n ≠ 0}. Todo inteiro é racional (n = 1).
- **Irracionais (𝕀):** números que não podem ser escritos como fração; sua forma decimal é infinita e não periódica.
- **Reais (ℝ):** união dos racionais e irracionais; representam quantidades contínuas, como 3,141592...

## Comparação de Conjuntos

- **Igualdade:** A = B quando todo elemento de A pertence a B e, reciprocamente, todo elemento de B pertence a A.

  A = B ⟺ ∀x | (x ∈ A → x ∈ B) ∧ (x ∈ B → x ∈ A)

- **Desigualdade:** A ≠ B quando existe um elemento de um dos conjuntos que não pertence ao outro.

  A ≠ B ⟺ ∃x | (x ∈ A ∧ x ∉ B) ∨ (x ∉ A ∧ x ∈ B)

## Subconjunto

A é subconjunto de B (A está contido em B) quando todo elemento de A também é elemento de B.

A ⊆ B ⟺ (x ∈ A → x ∈ B)

Se A não está contido em B, escrevemos A ⊈ B.

### Subconjunto próprio

Se A ⊆ B e A ≠ B, dizemos que A é subconjunto próprio de B e escrevemos A ⊂ B.

### Exemplos

Sejam A = {1, 7, 9, 15}, B = {7, 9} e C = {7, 9, 15, 20}:

- B ⊆ C, B ⊆ A e B ⊂ A
- A ⊄ C, pois 1 ∈ A e 1 ∉ C
- {7} ⊂ A e ∅ ⊆ C

### Propriedades

- **Reflexiva:** todo conjunto é subconjunto de si mesmo: A ⊆ A.
- **Transitiva:** (A ⊆ B) ∧ (B ⊆ C) → (A ⊆ C).
- **Conjunto vazio:** é subconjunto de qualquer conjunto: ∅ ⊆ A.

### Conjunto potência

O conjunto potência (ou conjunto das partes) de A, denotado 𝒫(A), é o conjunto de todos os subconjuntos de A. Se A tem n elementos, 𝒫(A) tem 2ⁿ elementos.

**Exemplo:** para A = {1, 2, 3}, 𝒫(A) = {∅, {1}, {2}, {3}, {1, 2}, {1, 3}, {2, 3}, {1, 2, 3}}, com 2³ = 8 elementos.

## Operações entre Conjuntos

- **União (A ∪ B):** elementos que pertencem a A ou a B.

  A ∪ B = {x ∈ U | (x ∈ A) ∨ (x ∈ B)}

- **Intersecção (A ∩ B):** elementos que pertencem a A e a B ao mesmo tempo.

  A ∩ B = {x ∈ U | (x ∈ A) ∧ (x ∈ B)}

- **Diferença (A − B):** elementos de A que não estão em B.

  A − B = {x ∈ U | (x ∈ A) ∧ (x ∉ B)}

- **Complemento (Aᶜ ou Ā):** tudo o que resta no universo ao retirar A.

  Aᶜ = {x ∈ U | x ∉ A} = {x | ¬(x ∈ A)}


## Leis da Álgebra dos Conjuntos

### Relação com as equivalências lógicas

Várias leis dos conjuntos correspondem a equivalências lógicas já conhecidas (∨ ↔ ∪, ∧ ↔ ∩, ¬ ↔ complemento, 1 ↔ U, 0 ↔ ∅):

| Equivalência lógica | Identidade de conjuntos |
| --- | --- |
| p ∨ 1 ≡ 1 | A ∪ U = U |
| p ∧ 0 ≡ 0 | A ∩ ∅ = ∅ |
| ¬(¬p) ≡ p | (Aᶜ)ᶜ = A |
| p ∧ (q ∨ r) ≡ (p ∧ q) ∨ (p ∧ r) | A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C) |
| p ∨ ¬p ≡ 1 | A ∪ Aᶜ = U |

### Principais leis

| Lei | Identidades |
| --- | --- |
| Elementos neutros | A ∪ ∅ = A; A ∩ U = A |
| Dominação | A ∪ U = U; A ∩ ∅ = ∅ |
| Idempotência | A ∪ A = A; A ∩ A = A |
| Comutativas | A ∪ B = B ∪ A; A ∩ B = B ∩ A |
| Associativas | (A ∪ B) ∪ C = A ∪ (B ∪ C); (A ∩ B) ∩ C = A ∩ (B ∩ C) |
| Distributivas | A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C); A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C) |
| Absorção | A ∪ (A ∩ B) = A; A ∩ (A ∪ B) = A |
| Duplo complemento (involução) | (Aᶜ)ᶜ = A |
| Complementares | A ∪ Aᶜ = U; A ∩ Aᶜ = ∅ |
| De Morgan | (A ∪ B)ᶜ = Aᶜ ∩ Bᶜ; (A ∩ B)ᶜ = Aᶜ ∪ Bᶜ |

## Cardinalidade

A cardinalidade de um conjunto A, denotada |A|, é o número de elementos de A. Por exemplo, A = {2, 4, 6} tem 3 elementos, logo |A| = 3.

**Exemplos**
- |{𝑎, 𝑏}| = 2
- |{𝑎, 𝑎}| = 1, pois elementos repetidos contam uma só vez
- |∅| = 0

## Produto Cartesiano

O produto cartesiano de A e B é o conjunto de todos os pares ordenados cujo primeiro elemento vem de A e o segundo vem de B:

A × B = {(a, b) | a ∈ A ∧ b ∈ B}

**Exemplo:** para A = {1, 2, 3, 4} e B = {2, 3}:
- A × B = {(1, 2), (2, 2), (3, 2), (4, 2), (1, 3), (2, 3), (3, 3), (4, 3)}
- B × A = {(2, 1), (2, 2), (2, 3), (2, 4), (3, 1), (3, 2), (3, 3), (3, 4)}

Para n conjuntos, o resultado é um conjunto de n-uplas:

A₁ × A₂ × ... × Aₙ = {(a₁, a₂, ..., aₙ) | a₁ ∈ A₁ ∧ a₂ ∈ A₂ ∧ ... ∧ aₙ ∈ Aₙ}

**Exemplo:** {a, b} × {1, 2} × {a, b} = {(a, 1, a), (a, 1, b), (a, 2, a), (a, 2, b), (b, 1, a), ..., (b, 2, b)}

**Propriedades**
- **Não comutativo:** em geral, A × B ≠ B × A.
- **Não associativo:** em geral, (A × B) × C ≠ A × (B × C).
