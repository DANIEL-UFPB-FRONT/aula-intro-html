## Modificar ícone ou marcador
Para modificar o ícone (ou marcador) de listas ordenadas (`<ol>`) e não ordenadas (`<ul>`) em HTML, você geralmente usará CSS. Aqui estão algumas maneiras de fazer isso:

### Para Listas Não Ordenadas (`<ul>`):

Você pode alterar o estilo do marcador usando a propriedade `list-style-type` em CSS. Existem vários valores predefinidos, como `disc`, `circle`, `square`, `none`, etc. Para um controle mais personalizado, você pode usar `list-style-image` para usar uma imagem como marcador.

**Exemplo com `list-style-type`:**

```html
<style>
    ul.custom {
        list-style-type: square; /* Ou 'circle', 'disc', 'none', etc. */
    }
</style>

<ul class="custom">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

**Exemplo com `list-style-image`:**

```html
<style>
    ul.custom {
        list-style-image: url('https://interactive-examples.mdn.mozilla.net/media/examples/rocket.svg');
    }
</style>

<ul class="custom">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

### Para Listas Ordenadas (`<ol>`):

As listas ordenadas são um pouco diferentes, pois elas normalmente exibem números ou letras. Para personalizar isso, você pode usar a propriedade `list-style-type`. Além dos tipos padrão (como `decimal`, `lower-alpha`, `upper-roman`, etc.), você pode usar o valor `none` e adicionar seu próprio estilo usando CSS e/ou JavaScript.

**Exemplo com `list-style-type`:**

```html
<style>
    ol.custom {
        list-style-type: upper-roman; /* Ou 'lower-alpha', 'decimal', 'lower-greek', etc. */
    }
</style>

<ol class="custom">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
```

Para um controle ainda mais personalizado, como ícones personalizados ou estilos complexos, você pode usar `list-style-type: none` para remover os marcadores padrão e, em seguida, adicionar estilos ou ícones personalizados usando CSS combinado com o pseudo-elemento `::before`.

**Exemplo com personalização avançada:**

```html
<style>
    ul {
            list-style: none; /* Remove o estilo default */
        }
    ul.custom li::before {
        content: "\2022"; /* Unicode para um marcador personalizado */
        margin-right:10px
    }
</style>

<ul class="custom">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

Este exemplo usa o pseudo-elemento `::before` para criar um marcador personalizado para cada item da lista. Você pode alterar o `content` para qualquer caractere ou ícone desejado (por exemplo, usando ícones de fonte como FontAwesome) e estilizá-lo conforme necessário.