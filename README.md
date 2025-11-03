# 🧭 Guia Essencial #01: Visão de Design da Página “Lista de Membros”

> **Este repositório NÃO contém código.**  
> Serve como guia de referência visual e funcional **antes da implementação**.

---

## ✅ Decisões Globais

### Fonte: **Raleway**
- Escolhida por sua limpeza, modernidade e boa hierarquia tipográfica.
- Disponível gratuitamente no Google Fonts (licença aberta).
- Uso recomendado:
  - Títulos: **Bold (700)**
  - Textos principais: **Regular (400)**
  - Textos secundários: **Light (300)**
  - Evitar itálico estilizado; preferir negrito + cor para ênfase.

---

## 📋 Status dos Componentes

| Nº | Componente               | Status     |
|----|--------------------------|------------|
| 1  | Cabeçalho (Header)       | ✅ Concluído |
| 2  | Breadcrumb               | ✅ Concluído |
| 3  | Título Principal         | ✅ Concluído |
| 4  | Conteúdo Principal       | ✅ Concluído |
| 5  | Paginação                | ⏳ Pendente |
| 6  | Rodapé (Footer)          | ⏳ Pendente |

> 🔁 Este documento será atualizado conforme avançamos.

---

# 🧭 Componente 1: Cabeçalho (Header)

## 🎯 Objetivo principal
Permitir identificação da marca, busca rápida e acesso a ações do usuário (menu, notificações etc.).

## 📐 Estrutura e Proporções (para desktop, largura ~1440px)

- **Altura total**: ~72px  
- **Logo**:
  - Alinhado à esquerda.
  - Altura: ~32px (proporcional ao texto “JUNTOS SOMOS+” em fonte bold, ~20–24px).
  - Margem direita: ~40px.
- **Barra de busca (central)**:
  - Largura: ~500px (ajustável entre 400–600px conforme viewport).
  - Altura: ~40px.
  - Arredondamento: 8px.
  - Ícone de lupa à esquerda (16x16px), padding interno de 12px.
  - Placeholder: “Buscar aqui” (cor cinza claro, \`#999\`).
- **Elementos à direita**:
  - Dois “placeholders” (podem ser botões ou ícones).
  - Tamanho: ~32x32px ou ~40x40px (círculos ou quadrados com borda arredondada).
  - Espaçamento entre eles: 16px.
  - Alinhados verticalmente ao centro do header.

## 🔄 Comportamento esperado
- Barra de busca: ao digitar, deve filtrar membros em tempo real (no futuro).
- Logo: clicável → retorna à página inicial.
- Elementos à direita: futuramente conterão ícones de perfil/notificação (com dropdown).

## 📱 Responsividade (visão geral)
- **Tablet**: busca reduz para ~300px; placeholders podem virar ícones.
- **Mobile**: logo + ícone de menu (hamburger); barra de busca aparece só ao clicar; placeholders entram no menu lateral.

---

# 🧭 Componente 2: Breadcrumb (Caminho de Navegação)

## 🎯 Objetivo principal
Mostrar ao usuário a **localização atual dentro da hierarquia do site**, permitindo navegação contextual e retorno fácil a páginas anteriores.

## 📐 Estrutura e Proporções (desktop, ~1440px)

- **Posicionamento**: logo abaixo do cabeçalho, alinhado à esquerda com o conteúdo principal.
- **Altura da linha**: ~24px
- **Fonte**: Raleway, **300 (Light)**, tamanho **14px**
- **Cor do texto**:
  - Páginas anteriores: \`#666\` (cinza médio)
  - Página atual: \`#333\` (cinza escuro) + **sem link**
- **Separadores**: símbolo \`>\` (ou \`/\`) em \`#999\`, com espaçamento de **8px** antes e depois
- **Exemplo visual**:
  \`\`\`
  Home > Usuários > Detalhes
  \`\`\`
  - “Home” e “Usuários”: links clicáveis
  - “Detalhes”: texto estático (página atual)

## 🔄 Comportamento esperado
- Cada parte do caminho (exceto a última) deve ser um **link funcional**.
- Ao passar o mouse: leve mudança de cor (ex: \`#007bff\` azul de acento) ou sublinhado sutil.
- Deve refletir **fielmente a estrutura lógica do site** (não apenas URLs).

## 📱 Responsividade
- **Desktop/Tablet**: exibido normalmente.
- **Mobile**: mantido, mas pode quebrar em múltiplas linhas se necessário (evitar truncamento).
- Em telas muito estreitas, opcionalmente exibir apenas o último nível com “...” (ex: \`... > Detalhes\`), mas **não recomendado** aqui — o breadcrumb é curto.

## 🎨 Alinhamento com Raleway
- Use **Light (300)** para suavidade visual — o breadcrumb é secundário, não deve competir com o título principal.
- Mantenha **espaçamento generoso** entre os elementos para evitar sensação de “aperto”.

---

# 🧭 Componente 3: Título Principal

## 🎯 Objetivo principal
Comunicar de forma **imediata e inequívoca** o propósito da página. Deve ser o primeiro elemento de conteúdo que o usuário lê após o cabeçalho e o breadcrumb.

## 📐 Estrutura e Proporções (desktop, ~1440px)

- **Texto**: “Lista de membros”
- **Posicionamento**: alinhado à esquerda, logo abaixo do breadcrumb, com margem superior de **24px**
- **Fonte**: Raleway, **700 (Bold)**  
- **Tamanho**: **28px** (pode escalar suavemente até 32px em telas maiores)
- **Cor**: \`#333\` (cinza escuro, para boa legibilidade e hierarquia)
- **Espaçamento abaixo (margin-bottom)**: **32px**  
  → Cria respiração entre o título e o conteúdo principal (filtros + grade)

## 🔄 Comportamento esperado
- **Estático**: não é interativo (não é link, não tem hover).
- Deve permanecer **sempre visível** na tela inicial (acima da dobra).

## 📱 Responsividade
- **Tablet**: mantém 28px, mas pode reduzir margin-bottom para 24px.
- **Mobile**:
  - Tamanho da fonte: **24px**
  - Margem superior: 20px
  - Margem inferior: 24px
  - Continua alinhado à esquerda (não centralizado)

## 🎨 Alinhamento com Raleway
- O uso de **Bold (700)** reforça autoridade visual sem parecer agressivo.
- A Raleway em tamanhos maiores tem boa presença graças às suas proporções abertas e altura-x generosa — ideal para títulos curtos como este.

## 💡 Nota de UX
- Evite adicionar ícones ou elementos decorativos ao título — a simplicidade reforça clareza.
- Se futuramente houver sub-título (ex: “Gerencie seus parceiros cadastrados”), ele viria em Raleway **400**, 18px, cor \`#666\`, com margin-top de 8px.

---

# 🧭 Componente 4: Conteúdo Principal

## 🎯 Objetivo principal
Permitir que o usuário **filtre membros por estado** e **navegue visualmente pelos perfis**, com clareza, eficiência e espaço adequado para expansão futura (ex: mais campos, ações por membro).

## 📐 Estrutura Geral (desktop, ~1440px)

- **Layout em duas colunas**:
  - **Sidebar (esquerda)**: largura fixa de **280px**
  - **Grade de membros (direita)**: ocupa o restante (`calc(100% - 300px)`, com 20px de gap)
- **Margem superior**: 0 (conecta-se diretamente ao título)
- **Espaçamento interno (padding)**: 24px à esquerda e direita no container (opcional, depende do alinhamento global)

## 🧩 Parte 4.1: Sidebar — Filtros por Estado

### Objetivo
Oferecer **filtragem por estado** de forma simples e escalável.

### Estrutura
- **Título**: “Por Estado”  
  - Raleway **600**, 18px, cor \`#444\`, margin-bottom: 16px
- **Checkboxes**:
  - Estilo personalizado (não nativo do browser)
  - Caixa do checkbox: 16x16px, borda \`1px solid #ccc\`, arredondamento 4px
  - Ao marcar: fundo \`#007bff\`, ícone de ✅ branco centralizado
  - Texto ao lado: Raleway **400**, 16px, cor \`#555\`, margin-left: 8px
  - Itens com padding vertical de 8px
- **Estados listados**:
  - São Paulo
  - Rio de Janeiro
  - Minas Gerais
  - Espírito Santo
  - Bahia
- **Link “Ver todos”**:
  - Raleway **500**, 15px, cor \`#007bff\`
  - Ao clicar: expande a lista completa de estados (funcionalidade futura)
  - Margin-top: 12px

### Comportamento
- Seleção múltipla permitida
- Ao marcar/desmarcar, a grade de membros **atualiza em tempo real**
- “Ver todos” pode abrir modal ou expandir inline (a definir)

### Responsividade
- **Tablet (até 1024px)**: sidebar vira **acordeão** (colapsável) ou se move para **filtro superior** (botão “Filtrar” que abre drawer)
- **Mobile**: filtros entram em **modal ou drawer lateral**, liberando 100% da tela para a grade

## 🧩 Parte 4.2: Grade de Membros

### Objetivo
Exibir perfis de forma **legível, escaneável e consistente**.

### Estrutura da Grade
- **Layout**: CSS Grid (3 colunas em desktop)
- **Gap**: 24px entre cards
- **Cards por linha**: 3 (desktop), 2 (tablet), 1 (mobile)
- **Largura do card**: \`100%\` (dentro da coluna do grid)

### Estrutura do Card
- **Altura**: ~160px (ajustável conforme conteúdo)
- **Borda**: \`1px solid #eee\`, bordas arredondadas 8px
- **Sombra sutil**: \`box-shadow: 0 2px 6px rgba(0,0,0,0.05)\` (opcional)
- **Padding interno**: 16px

### Conteúdo do Card
1. **Avatar**:
   - Tamanho: 40x40px
   - Formato: círculo (\`border-radius: 50%\`)
   - Cor de fundo: \`#e0e0e0\`
   - Ícone genérico de pessoa (SVG ou emoji 👤)
2. **Nome**:
   - Raleway **600**, 18px, cor \`#333\`, margin-top: 8px
3. **Endereço**:
   - Raleway **400**, 15px, cor \`#555\`, margin-top: 4px
   - Formato:  
     \`Rua Exemplo, 123\`  
     \`Cidade - SP, 12345-678\`
4. **Placeholders (linhas cinzas)**:
   - Representam campos futuros (ex: “Representante”, “(11) 99999-9999”)
   - Altura: 12px, largura variável, fundo \`#f0f0f0\`, borda arredondada 4px
   - Margin-top: 8px

### Comportamento
- Cada card **não é clicável por padrão**, mas pode ter um botão “Ver detalhes” no futuro
- Ao aplicar filtros, **os cards não correspondentes desaparecem com animação suave**

### Responsividade
- **Desktop**: 3 colunas
- **Tablet (768px–1023px)**: 2 colunas
- **Mobile (<768px)**: 1 coluna, cards com padding horizontal ajustado

## 🎨 Alinhamento com Raleway
- Hierarquia clara:
  - Nome: **600** → destaque
  - Endereço: **400** → informação secundária
  - Placeholders: não usam texto, mas se tiverem, seriam **300**
- A Raleway permite **alta densidade de informação sem poluição visual**

## 💡 Notas de UX
- Evitar sobrecarregar o card — o foco é **nome + localização**
- Filtros devem ser **persistentes** (se o usuário atualizar, os estados selecionados permanecem)
- Número de itens exibidos: **9 por página** (3×3), conforme layout original

---

<!-- Próximos componentes serão adicionados aqui -->