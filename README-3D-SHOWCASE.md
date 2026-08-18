# Showcase 3D da Dumas

Esta seção foi preparada para um showcase 3D guiado pelo scroll com Three.js, GSAP e ScrollTrigger.

## Assets esperados

Coloque os arquivos nestes caminhos:

```text
models/product.glb
textures/front.webp
textures/back.webp
```

O GLB deve conter meshes chamados `Front` e `Back`, ambos com UVs válidos. A arte das faces usa as texturas como `material.map`; o alpha mistura a arte com a cor base do material, sem recortar ou furar o mesh.

## Como funciona

- O canvas é transparente e ocupa o viewport da seção.
- O ScrollTrigger só envia o progresso de `0` a `1`.
- A cena interpola o `group` em três fases: entrada, giro e saída.
- O RAF é ativado somente enquanto a seção está em reprodução.
- `prefers-reduced-motion` mantém o produto estático.
- Se os assets ainda não existirem, a página usa uma prévia visual de fallback e não exibe erro.

## O que preciso receber

1. `product.glb` final, com as meshes `Front` e `Back`.
2. `front.webp` e `back.webp`, preferencialmente com alpha quando a arte não ocupar todo o retângulo.
3. Uma confirmação de qual cor base deve aparecer nas áreas transparentes do produto.

Depois de receber os arquivos, basta colocá-los nas pastas indicadas e testar a seção `/experiencia-3d` na página.
