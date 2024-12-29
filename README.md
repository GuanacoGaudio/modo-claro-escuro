# Modo Claro/Escuro: Acessibilidade e Boas Práticas na Web

## Introdução
Você já deve ter visto sites ou aplicativos que oferecem a opção de alternar entre modo claro e escuro. Parece simples, mas essa funcionalidade vai além de uma questão de estilo. Trata-se de uma prática de acessibilidade que melhora a experiência de diversos usuários.

Este artigo explora os motivos para implementar o modo claro/escuro e como fazer isso com código limpo, funcional e acessível.

---

## Por que adotar o modo claro/escuro?

### Acessibilidade aprimorada
Muitas pessoas enfrentam dificuldades visuais, como sensibilidade à luz ou fotofobia. O modo escuro reduz o cansaço visual, enquanto o modo claro proporciona melhor legibilidade em ambientes bem iluminados.

### Conforto e personalização
Dar aos usuários controle sobre como consomem conteúdo digital melhora a usabilidade e aumenta o tempo de permanência no site.

### Inclusão e responsabilidade social
Empresas que adotam práticas acessíveis demonstram respeito por todos os usuários, criando uma experiência digital universal.

---

## Como funciona?

Implementamos o modo claro/escuro sem bibliotecas externas, utilizando apenas HTML, CSS e JavaScript nativos. Isso torna o código leve, eficiente e fácil de integrar em qualquer projeto.

---

## Exemplo prático

### HTML
```html
<button class="mode-switch" onclick="toggleDarkMode()">🌙</button>
```
O botão é simples e intuitivo, com um ícone representando o tema atual.

### CSS
```css
body {
    transition: background-color 0.3s ease, color 0.3s ease;
}

body.dark-mode {
    background-color: #121212;
    color: #E0E0E0;
}

.mode-switch {
    position: fixed;
    top: 20px;
    right: 20px;
    padding: 10px;
    background-color: #2B77A4;
    color: white;
    border-radius: 50%;
    cursor: pointer;
    font-size: 1.5rem;
    animation: pulse 1.5s infinite;
}

@keyframes pulse {
    0%, 100% {
        box-shadow: 0 0 10px rgba(43, 119, 164, 0.5);
    }
    50% {
        box-shadow: 0 0 20px rgba(43, 119, 164, 0.9);
    }
}
```
Os estilos oferecem uma transição suave entre os temas e garantem um botão visualmente agradável com animação.

### JavaScript
```javascript
function toggleDarkMode() {
    document.body.classList.toggle('dark-mode');
}
```
O script adiciona ou remove a classe `dark-mode` no elemento `<body>`, alternando entre os estilos definidos no CSS.

---

## Como implementar no seu projeto

1. Copie e cole os exemplos acima no seu código.
2. Customize cores e estilos para se adequar à identidade visual do seu site.
3. Teste em dispositivos diferentes para garantir uma experiência consistente.

---

## Boas práticas

### Mobile first
Garanta que o design se adapta bem a telas menores antes de pensar em telas maiores.

### Evite sobrecarregar o usuário
Ofereça uma interface simples e opções claras de alternância.

### Teste a acessibilidade
Use ferramentas como o Lighthouse ou WAVE para verificar se o seu site está realmente acessível.

---

## Conclusão

O modo claro/escuro é uma funcionalidade acessível, útil e bem-vista por usuários. Implementá-lo não é apenas uma questão de estilo, mas um passo importante para tornar o mundo digital mais inclusivo.

Está na hora de repensar como seus projetos podem beneficiar mais pessoas. Adicione o modo claro/escuro e mostre que você se importa com todos os seus usuários!
