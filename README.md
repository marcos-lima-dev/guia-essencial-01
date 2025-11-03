cat > README.md << 'EOF'
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
| 4  | Conteúdo Principal       | ⏳ Pendente |
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

<!-- Próximos componentes serão adicionados aqui -->
EOF