# Cores, Gradientes e Efeitos Visuais no CSS

CSS moderno não atua apenas como estilização.
Atualmente ele participa diretamente de:
- experiência do usuário;
- hierarquia visual;
- acessibilidade;
- percepção de qualidade;
- identidade visual.

---

# 1. Formatos de Cores Modernos

- **HEX**
- **HSL**
- **OKLCH**

HEX representa cores em hexadecimal.

RGB representa intensidade luminosa.

HSL organiza cor por:
- matiz;
- saturação;
- luminosidade.

OKLCH é um espaço de cor perceptualmente uniforme.
Mudanças numéricas geram mudanças visuais mais consistentes.

```css
:root{
  --primaria:#1e3c72;
  --destaque:hsl(210 80% 60%);
  --moderna:oklch(62% 0.22 260);
}

body{
  background:#0f172a;
  color:var(--destaque);
}
```

---

# 2. Gradientes Lineares

- **linear-gradient**
- **color-stops**
- **renderização dinâmica**

Gradientes são tratados pelo navegador como imagens geradas dinamicamente.

O linear-gradient cria transições contínuas entre cores.

Color-stops controlam posição e distribuição das cores.

```css
body{
  min-height:100vh;

  background:
    linear-gradient(
      135deg,
      #1e3c72 0%,
      #2a5298 50%,
      #4facfe 100%
    );
}
```

---

# 3. Gradientes Radiais e Cônicos

- **radial-gradient**
- **conic-gradient**
- **profundidade visual**

Gradientes radiais expandem cores a partir de um ponto central.

Gradientes cônicos distribuem cores em rotação angular.

São muito usados em:
- dashboards;
- gráficos;
- iluminação;
- interfaces modernas.

```css
.card{
  background:
    radial-gradient(
      circle at top,
      rgba(255,255,255,0.3),
      rgba(15,23,42,1)
    );
}

.chart{
  background:
    conic-gradient(
      #22c55e 0deg,
      #3b82f6 180deg,
      #ef4444 360deg
    );
}
```

---

# 4. Sombras e Profundidade

- **box-shadow**
- **drop-shadow**
- **transparência**

Sombras adicionam profundidade e hierarquia visual.

box-shadow utiliza a caixa retangular do elemento.

filter: drop-shadow() considera transparência real da renderização.

```css
.card{
  box-shadow:
    0 10px 30px rgba(0,0,0,0.25);
}

.logo{
  filter:
    drop-shadow(
      0 0 12px rgba(59,130,246,0.7)
    );
}
```

---

# 5. Opacidade e Filtros Visuais

- **opacity**
- **blur**
- **GPU**

opacity afeta o elemento inteiro, incluindo filhos.

Filtros aplicam pós-processamento visual após renderização.

blur() e brightness() podem utilizar aceleração gráfica.

```css
.modal{
  opacity:0.8;
}

.glass{
  backdrop-filter:blur(12px);
}

.image{
  filter:brightness(1.2);
}
```

---

# 6. Boas Práticas e Acessibilidade

- **WCAG**
- **contraste**
- **performance**

Interfaces modernas precisam manter:
- legibilidade;
- contraste adequado;
- baixo custo de renderização.

Excesso de blur e sombras pode aumentar repaint e custo gráfico.

```css
body{
  background:#111827;
  color:#f9fafb;
}

button{
  background:#2563eb;
  color:white;
}
```

---

# Conclusão

CSS moderno permite criar interfaces sofisticadas sem depender excessivamente de imagens externas.

Cores, gradientes e efeitos visuais participam diretamente de:
- acessibilidade;
- identidade visual;
- experiência do usuário;
- percepção de qualidade;
- design systems modernos.
