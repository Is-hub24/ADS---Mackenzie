# 🌱 Plataforma de Pontos de Descarte — Interface Renovada

Esta é uma **versão totalmente redesenhada** da interface de Pontos de Descarte, criada do zero com foco em simplicidade, modernidade, acessibilidade e expansão futura. Não segue o layout, estilo ou estrutura do repositório original — é um projeto realmente **novo**, mantendo apenas a ideia base.

---

## ✨ O que esta versão traz de novo

### 🎨 Visual Moderno e Minimalista

* Tema escuro elegante com destaques em verde.
* Layout em cards responsivos.
* Espaço inteligente para listar pontos, buscar e gerenciar.

### ⚡ Funcionalidades Aprimoradas

* Busca inteligente em tempo real.
* Favoritos persistidos no navegador.
* Estatísticas dinâmicas sobre pontos cadastrados.
* Sistema de cadastro e edição totalmente em modal.
* Estrutura pronta para integrar com APIs reais.

### 🗺️ Mapa Integrável

A interface possui um container dedicado para mapas, mas **não usa nenhuma biblioteca por padrão**, permitindo que você escolha:

* Leaflet (recomendado)
* Mapbox
* Google Maps

Posso integrar qualquer opção para você.

---

## 🧩 Estrutura do Projeto

```
index.html   → Estrutura da página
style.css    → Estilos modernos (opcional caso separado)
app.js       → Lógica de filtros, favoritos, cadastro e armazenamento
```

Atualmente, tudo está em um único arquivo, mas posso separar se preferir.

---

## 🚀 Como Executar

### Opção 1 — Abrir diretamente

Abra o arquivo `index.html` no navegador.

### Opção 2 — Live Server

* Abra a pasta no VS Code
* Clique com o botão direito em `index.html`
* Selecione **Open with Live Server**

---

## 🔌 Integrando com Backend

Para consumir dados reais de API, basta substituir o carregamento inicial:

```js
state.points = loadPointsFromStorage() || SAMPLE;
```

por:

```js
fetch("URL_DA_SUA_API/pontos")
  .then(r => r.json())
  .then(data => {
    state.points = data;
    renderList();
  });
```

Precisa que eu faça a integração completa? É só pedir.

---

## 📈 Estatísticas Automáticas

A interface calcula e exibe:

* Total de pontos cadastrados
* Total de favoritos
* Quantidade de cidades

Tudo é atualizado em tempo real conforme você cadastra ou edita.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5** (estrutural)
* **CSS3** (visual clean e responsivo)
* **JavaScript Vanilla** (sem frameworks)
* **localStorage** (persistência simples)

---

## 🌐 Deploy

### GitHub Pages

1. Vá em *Settings > Pages*
2. Seleciona branch **main**
3. Folder: “root”

### Vercel / Netlify

* Importar repositório
* Deploy automático

Posso configurar o deploy para você também.

---

## 🤝 Colaboração

Contribuições são bem-vindas: novas telas, novas integrações, melhorias de performance ou UX.

Se quiser, posso preparar:

* `CONTRIBUTING.md`
* `LICENSE`
* `CHANGELOG`
* Padrão de commits (Conventional Commits)

---

## 📝 Objetivo do Projeto

Criar uma interface prática e limpa para visualizar, filtrar e cadastrar pontos de descarte, útil para projetos acadêmicos, protótipos ou integração com APIs reais.

Se quiser expandir para aplicativo mobile híbrido, dashboard administrativo ou tema claro/escuro, posso desenvolver as próximas telas.
