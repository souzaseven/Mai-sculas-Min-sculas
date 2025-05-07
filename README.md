# 🔠 Conversor de Maiúsculas e Minúsculas

Uma ferramenta web simples para converter textos entre maiúsculas, minúsculas e capitalização de primeira letra.
<!--
![Preview do Conversor](https://raw.githubusercontent.com/souzaseven/Site2/Desafios/icon%20eu.ico)
-->
## ✨ Funcionalidades

- **Conversão Instantânea**:
  - Texto em MAIÚSCULAS
  - Texto em minúsculas
  - Primeira Letra de Cada Palavra Maiúscula
  - Atualização em tempo real

- **Recursos Úteis**:
  - Cópia fácil para área de transferência
  - Limpeza rápida dos campos
  - Interface intuitiva e responsiva
  - Feedback visual ao copiar

## 🛠️ Tecnologias Utilizadas

- **Frontend**:
  - HTML5 semântico
  - CSS3 moderno
  - JavaScript puro (ES6+)

- **Bibliotecas**:
  - Font Awesome (ícones)
  - Google Analytics (métricas)
  - Google AdSense (monetização)

## 📂 Estrutura de Arquivos
conversor-maiusculas/ <br>
├── maiuscula-minuscula.html # Página principal <br>
├── style.css # Estilos personalizados <br>
└── script.js # Lógica do conversor <br>
 <br>
 
## 🎨 Design e Interface

- **Tema Azul Moderno**:
  - Fundo azul (#007bff)
  - Área branca para conteúdo
  - Sombras e bordas arredondadas

- **Layout Organizado**:
  - Campos de texto espaçosos
  - Opções claras de conversão
  - Botões de ação visíveis

- **Interações**:
  - Efeitos hover nos botões
  - Transições suaves
  - Feedback ao copiar

## ⚙️ Como Funciona

### Conversão de Texto
```javascript
function converterTexto() {
    const tipo = document.querySelector('input[name="tipo"]:checked').value;
    let resultado;
    
    switch(tipo) {
        case 'maiusculas':
            resultado = texto.toUpperCase();
            break;
        case 'minusculas':
            resultado = texto.toLowerCase();
            break;
        case 'primeiraletra':
            resultado = texto.split(' ').map(palavra => 
                palavra.charAt(0).toUpperCase() + palavra.slice(1).toLowerCase()
            ).join(' ');
            break;
    }
    
    document.querySelector('.destino').value = resultado;
}
```
### Cópia do Texto
```javascript
function copiarTexto() {
    const textoConvertido = document.querySelector('.destino');
    textoConvertido.select();
    document.execCommand('copy');
    alert('Texto copiado!');
}
```
### Cópia do Texto💡 Dicas de Uso 
Para converter rapidamente:
Digite ou cole o texto
Selecione o tipo de conversão
O resultado aparece instantaneamente

### Personalização:
```css
/* Para mudar o tema */
body {
    background-color: #2c3e50;
}
.container {
    background-color: #ecf0f1;
}
```
### Para adicionar mais opções:
```javascript
case 'invertido':
    resultado = texto.split('').map(letra => 
        letra === letra.toUpperCase() ? 
        letra.toLowerCase() : 
        letra.toUpperCase()
    ).join('');
    break;
```

## 📝 Exemplos

- **Original**: hello world
- **Maiúsculas**: HELLO WORLD
- **Minúsculas**: hello world
- **Primeira Letra**: Hello World
