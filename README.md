# JPEG Image Compression

Este projeto implementa um codec de compressão JPEG básico, utilizando técnicas como Transformada Discreta do Cosseno (DCT), quantização, e codificação de Huffman. O objetivo é fornecer uma implementação prática dos principais componentes do processo de compressão JPEG.

## Sumário

1. [Visão Geral](#visão-geral)
2. [Pré-requisitos](#pré-requisitos)
3. [Estrutura do Projeto](#estrutura-do-projeto)
4. [Como Usar](#como-usar)
5. [Exemplos](#exemplos)
6. [Contribuição](#contribuição)
7. [Licença](#licença)

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

## Estrutura do Projeto

O projeto é estruturado da seguinte forma:

- `compressao_jpeg.py`: Contém a implementação principal do codec JPEG.
- `quantizacao.py`: Define a função de quantização e as matrizes utilizadas.
- `codificacao_huffman.py`: Implementa a codificação de Huffman.
- `testes.py`: Scripts de teste para verificar a funcionalidade do codec.
- `exemplos/`: Pasta com imagens de exemplo e scripts para visualização.

## Como Usar

1. **Carregar a Imagem**: Carregue a imagem que deseja comprimir.
2. **Converter para YCbCr**: Converta a imagem para o espaço de cores YCbCr.
3. **Aplicar Transformada DCT**: Use a DCT para converter a imagem para o domínio da frequência.
4. **Quantizar os Coeficientes**: Aplique a quantização usando as tabelas JPEG.
5. **Codificar com Huffman**: Codifique os dados quantizados com Huffman.
6. **Salvar como Arquivo JPEG**: Escreva o arquivo JPEG com os dados comprimidos.

**Exemplo de uso**:

```python
import numpy as np
import matplotlib.pyplot as plt
from compressao_jpeg import compressao_jpeg

# Carregar imagem
imagem = plt.imread('imagem_exemplo.png')

# Compressão JPEG
jpeg_data = compressao_jpeg(imagem, qualidade=95)

# Salvar imagem JPEG
with open('imagem_comprimida.jpg', 'wb') as f:
    f.write(jpeg_data)
```

