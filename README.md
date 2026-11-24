# UNIVERSUM

Experiência narrativa e visual para investigar a evolução do Universo.

## Requisitos

- Node.js 20.19+ ou 22.12+
- npm

## Instalação

```bash
npm install
npm run dev
```

## Scripts

```bash
npm run dev
npm run typecheck
npm run build
npm run preview
```

## Estrutura

```text
src/
├── components/       # cena 3D, narrativa e modal científica
├── data/             # capítulos da experiência
├── physics/          # cálculos físicos isolados da interface
├── styles/           # estilos globais e responsividade
├── App.tsx
└── main.tsx
```

## Rolagem e transições — v0.1.2

A linha do tempo é medida pela própria coluna narrativa, do início ao fim dela. Isso mantém a mesma referência no desktop e no mobile. Os marcos são sincronizados em uma única escala: plasma primordial, expansão e resfriamento, e a faixa térmica associada ao crossover quark-hádrons.

A cena mantém as mesmas partículas durante toda a sequência. O fator de expansão aumenta continuamente, a câmera recua com a distribuição e, perto do crossover, os pontos se agrupam gradualmente em regiões visuais. Não há troca de cena. A contração dos pontos é uma metáfora gráfica de agrupamento/confinamento, não uma simulação de QCD.

## Limites científicos

O motor usa uma aproximação de Universo dominado por radiação:

- `a(t) / a₀ = sqrt(t / t₀)`
- `T(t) / T₀ = a₀ / a(t)`
- `H(t) = 1 / (2t)`

O intervalo demonstrado é de `10⁻⁶` a `10⁻⁴` segundos. A normalização de temperatura de `10¹³ K` em `10⁻⁶ s` é didática e não substitui uma tabela termodinâmica calibrada nem uma integração completa das equações de Friedmann.

A visualização de partículas é uma representação procedural. Ela não resolve numericamente a cromodinâmica quântica nem simula colisões reais.

## Próximas evoluções recomendadas

1. Adicionar testes unitários para `calculateCosmology`.
2. Substituir a normalização didática por uma parametrização documentada.
3. Implementar integração configurável das equações de Friedmann.
4. Separar a transição QGP-hádrons em um modelo térmico com parâmetros de referência.
5. Adicionar controles de pausa, velocidade e navegação temporal.
6. Implementar acessibilidade completa e fallback 2D para dispositivos sem WebGL.

## Diretriz editorial

A interface prioriza explicações físicas diretas: condição inicial, processo, consequência e limites do modelo. Cada etapa deve separar resultados calculados de representações conceituais.
