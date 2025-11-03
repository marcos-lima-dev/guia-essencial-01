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
| 2  | Breadcrumb               | ⏳ Pendente |
| 3  | Título Principal         | ⏳ Pendente |
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
  - Placeholder: “Buscar aqui” (cor cinza claro, `#999`).
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

<!-- Próximos componentes serão adicionados aqui -->