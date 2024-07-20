# Trabalho Final - Processamento de sinais

Insituto Federal de Minas Gerais - IFMG - Campus Betim

Gabriel Keven Domingues de Souza - RA: 0056232

Victor Hugo Bittencourt - RA: 0055966

## Introdução

Este projeto implementa um codec de compressão JPEG básico, utilizando técnicas como Transformada Discreta do Cosseno (DCT), quantização, e codificação de Huffman. O objetivo é fornecer uma implementação prática dos principais componentes do processo de compressão JPEG.

## Sumário

1. [Visão Geral](#visão-geral)
2. [Pré-requisitos](#pré-requisitos)
3. [Como Usar](#como-usar)
4. [Exemplos](#exemplos)

## Visão Geral

O projeto realiza a compressão de imagens JPEG seguindo os principais passos:

1. **Transformada Discreta do Cosseno (DCT)**: Converte a imagem do domínio espacial para o domínio da frequência.
2. **Quantização**: Reduz a precisão dos coeficientes DCT usando tabelas de quantização.
3. **Codificação de Huffman**: Codifica os dados quantizados usando a técnica de Huffman para compressão adicional.
4. **Criação de Arquivo JPEG**: Constrói um arquivo JPEG com os dados comprimidos e os cabeçalhos necessários.

## Pré-requisitos

Certifique-se de que você tenha os seguintes pacotes Python instalados:

- `numpy`
- `matplotlib`
- `bitstream` (para manipulação de bits)
- `huffman` (para codificação de Huffman)

Você pode instalar essas dependências usando o pip:

```bash
pip install numpy matplotlib bitstream huffman
```

## Como Usar

1. **Carregar a Imagem**: Carregue a imagem que deseja comprimir.
2. **Converter para YCbCr**: Converta a imagem para o espaço de cores YCbCr.
3. **Aplicar Transformada DCT**: Use a DCT para converter a imagem para o domínio da frequência.
4. **Quantizar os Coeficientes**: Aplique a quantização usando as tabelas JPEG.
5. **Codificar com Huffman**: Codifique os dados quantizados com Huffman.
6. **Salvar como Arquivo JPEG**: Escreva o arquivo JPEG com os dados comprimidos.

## Exemplos

![image](https://github.com/user-attachments/assets/73960f4c-c985-48d9-b0f7-290c4db1df30)


