---
title: "Complexidade de Kolmogorov"
date: 2023-02-19
draft: false
tags: ["Computação", "Teoria da Informação", "Algoritmos", "Ciência de Dados"]
categories: ["Computação"]
description: "Uma introdução à Complexidade de Kolmogorov, também conhecida como complexidade algorítmica da informação, e sua importância para a ciência de dados e teoria da informação."
cover:
  image: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgD3YKiWBJRXWYY6Pq7PN72kwuwXb_pbKhNxNZ0V2TWjNOYEwAR8-DpD8CWWSH_vR72Q4mT9_8sNxr8b87u4iiydYWRIMu3NxY8GtpgFuJzifP-owpMpqrlsjBJDP4TIDO1T82_uSkwVxtn6or5RWuKfciPK4fgHEL_OEoh9ud_Wo9qy7v_OPZUtTZh/s883/binary-tape-blur.png"
  alt: "Fita binária desfocada"
canonical: "https://ronymarcolino.blogspot.com/2023/02/complexidade-de-kolmorogov.html"
---

Complexidade de Kolmogorov, também conhecida como complexidade algorítmica da informação, é uma medida da quantidade de informações contidas em uma cadeia de caracteres. É definida como a extensão do programa mais curto possível que pode ser escrito em uma linguagem de programação para gerar uma determinada cadeia de caracteres. Em outras palavras, é uma medida (proporcional) da quantidade mínima de informação necessária para descrever uma cadeia de caracteres.

É baseado na ideia de que se uma dada sequência **S** pode ser gerada por um algoritmo menor que o comprimento da sequência dada, então **S** pode ser considerada uma sequência aleatória. A ideia básica é que qualquer sequência de caracteres pode ser comprimida em sua forma mais eficiente e a complexidade de Kolmogorov de uma sequência é do tamanho do programa mais curto necessário para gerá-la — a chamada **Descrição de Menor Comprimento** (do inglês *Minimum Description Length*).

![Fita binária desfocada](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgD3YKiWBJRXWYY6Pq7PN72kwuwXb_pbKhNxNZ0V2TWjNOYEwAR8-DpD8CWWSH_vR72Q4mT9_8sNxr8b87u4iiydYWRIMu3NxY8GtpgFuJzifP-owpMpqrlsjBJDP4TIDO1T82_uSkwVxtn6or5RWuKfciPK4fgHEL_OEoh9ud_Wo9qy7v_OPZUtTZh/s883/binary-tape-blur.png)

Essa abordagem fornece uma medida teórica da quantidade de informação contida em uma cadeia de caracteres e pode ser usada para comparar a complexidade de diferentes cadeias. Entretanto, é importante notar que a complexidade de Kolmogorov não é uma medida prática e não pode ser computada diretamente (em termos numéricos) para uma determinada cadeia de caracteres.

## Exemplos Introdutórios

Por exemplo, considere a cadeia de caracteres `"olá mundo"`. Esta cadeia (de tamanho 9) pode ser gerada por um programa que simplesmente imprime os caracteres `"olá mundo"` na tela. A complexidade de Kolmogorov desta cadeia teria o mesmo comprimento deste programa (que é relativamente curto).

Por outro lado, considere uma cadeia que contenha uma abundância de dados aleatórios. A complexidade de Kolmogorov desta cadeia seria muito maior, porque exigiria um programa mais longo para gerá-la. Em geral, as cadeias com alta complexidade de Kolmogorov são consideradas mais complexas e contêm mais informações do que as cadeias com baixa complexidade.

Outro exemplo muito interessante é o do **número pi**: ele é um número irracional com infinitas casas decimais, porém existem algoritmos que conseguem gerar quantas casas decimais forem solicitadas com baixo erro e com relativa simplicidade, como o dos irmãos David e Gregory Chudnovsky [[1]](https://brasil.elpais.com/brasil/2018/03/14/ciencia/1521011921_905686.html).

## Compressão de Cadeias

Para entender este conceito mais claramente, vamos olhar para um exemplo em que é possível comprimir uma cadeia. Suponha que temos duas cadeias de tamanho `n = 8`:

- Primeira cadeia: `x  = 01010101`
- Segunda cadeia:  `x' = 11101001`

Para a primeira cadeia, podemos criar um programa de tamanho 4 (ou `n/2`) que irá gerá-la. Em Python, o programa poderia ser algo parecido com:

```python
print("01" * 4)
```

Porém, para a segunda cadeia teremos algo como a impressão literal da própria cadeia:

```python
print("11101001")
```

## Aleatoriedade e o Conjunto R

Podemos definir um conjunto de strings aleatórias **R** da seguinte forma:

> **R = {x | K(x) ≥ |x|}**

Neste caso, uma cadeia é considerada aleatória se o tamanho do menor programa que a pode gerar for maior ou igual ao tamanho da própria cadeia. Esta definição de aleatoriedade pode ser bastante satisfatória, pois demonstra que uma cadeia de caracteres é aleatória se não conseguirmos criar um padrão inteligente para descrevê-la ou gerá-la.

No entanto, esta noção de aleatoriedade acaba se tornando fundamentalmente problemática. Não é possível chegar a um algoritmo geral para encontrar este conjunto **R** e determinar se um dado **x** é aleatório. Este resultado é conhecido como o **Teorema da Incompletude de Kolmogorov**.

## Relevância para Ciência de Dados

A complexidade de Kolmogorov é um conceito muito importante para a ciência de dados e para a teoria da informação. Ele pode ser usado para classificar dados em termos de complexidade. A compreensão deste conceito pode ajudar os cientistas de dados a tomar melhores decisões quando se trata de comprimir dados ou criar algoritmos para gerá-los.

## Referências

1. [Algoritmo de Chudnovsky — El País Brasil](https://brasil.elpais.com/brasil/2018/03/14/ciencia/1521011921_905686.html)
2. [Os primórdios da Teoria da Complexidade de Kolmogorov — NE10](https://ne10.uol.com.br/canal/coluna/difusao/noticia/2012/04/02/os-primordios-da-teoria-da-complexidade-de-kolmogorov---parte-i-335412.php)
3. [An Introduction to Kolmogorov Complexity and Its Applications — CWI (PDF)](https://homepages.cwi.nl/~paulv/papers/handbooklogic07.pdf)
