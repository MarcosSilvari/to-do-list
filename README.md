# 📝 To-Do List

Lista de tarefas feita com **HTML, CSS e JavaScript puro**, com tema escuro e efeitos neon roxo/magenta. As tarefas ficam salvas no navegador, então continuam lá mesmo depois de recarregar ou fechar a página.

## ✨ Funcionalidades

- Adicionar novas tarefas
- Ignorar tarefas vazias (validação do campo)
- Marcar/desmarcar tarefa como concluída ao clicar nela (texto riscado)
- Excluir tarefas individualmente
- Salvar tudo automaticamente no `localStorage` (as tarefas e o estado de concluída persistem ao recarregar)

## 🛠️ Tecnologias

- **HTML5**: estrutura da página
- **CSS3**: estilização, tema escuro e efeitos de brilho (glow) com neon roxo/magenta
- **JavaScript (ES6)**: lógica, manipulação do DOM e persistência de dados
- **localStorage**: armazenamento no próprio navegador, sem backend nem banco de dados

## 📁 Estrutura do projeto

```
todo-list/
├── index.html
└── FRONTEND/
    ├── CSS/
    │   └── list.css
    └── JS/
        └── list.js
```

## 🚀 Como executar

1. Baixe ou clone o projeto
2. Abra o arquivo `index.html` no navegador (é só dar dois cliques, não precisa de servidor)
3. Digite uma tarefa, clique em **Adicionar** e pronto

## ⚙️ Como funciona

- As tarefas ficam guardadas num array de objetos no formato `{ texto: "...", concluida: false }`
- A cada mudança (adicionar, concluir ou excluir), o array é convertido para texto com `JSON.stringify()` e salvo no `localStorage`
- Quando a página abre, o `JSON.parse()` lê esse texto de volta e a função `criarTarefaNaTela()` desenha cada tarefa salva
- O clique no botão **Excluir** usa `event.stopPropagation()` para não disparar também o clique de "concluir" da tarefa

## 📚 Conceitos praticados

- Seleção de elementos com `getElementById`
- Criação e inserção de elementos com `createElement` e `appendChild`
- Eventos com `addEventListener` e o comportamento de *event bubbling*
- Manipulação de classes com `classList.toggle`
- Arrays: `push`, `filter` e `forEach`
- Persistência de dados com `localStorage`, `JSON.stringify` e `JSON.parse`

## 🔮 Melhorias futuras

- Adicionar tarefa apertando **Enter**
- Editar o texto de uma tarefa já criada
- Filtros (todas / pendentes / concluídas)
- Integrar com backend e banco de dados para salvar as tarefas na conta do usuário

## 👤 Autor

**Marcos Silvari**, estudante de Análise e Desenvolvimento de Sistemas (ADS) na Cruzeiro do Sul.
