O **OCR (Optical Character Recognition)** é uma tecnologia de **visão computacional** que permite transformar **texto presente em imagens** (fotos, PDFs escaneados, frames de vídeo etc.) em **texto digital editável**.

Em outras palavras, ele responde à pergunta:

> “Como fazer um computador **ler texto que está dentro de uma imagem**?”

Isso é fundamental para automação de documentos, leitura de placas, digitalização de arquivos e aplicativos mobile.

O processo ocorre em etapas:

## Pré-processamento da imagem 

A imagem é tratada para facilitar a leitura.

Técnicas comuns:
**Binarização** : Transforma a imagem em preto e branco.
**Remoção de ruído**: Remove manchas e artefatos.
**Correção de inclinação**: Endireita textos tortos.
**Normalização de contraste**: Melhora visibilidade das letras.

Bibliotecas comuns:
- OpenCV
- Pillow
- scikit-image

Então ocorre a 

## Detecção de regiões de texto

Antes de reconhecer letras, o sistema precisa descobrir:
 Onde existe texto na imagem?

Isso pode ser feito com:
### Métodos clássicos
- análise de bordas
- connected components
### Métodos modernos (Deep Learning)

- EAST text detector
- CRAFT
- YOLO para texto

## Segmentação

Cada linha ou palavra é separada.

RECIBO  
↓  
R E C I B O

Algoritmos identificam:

- linhas
- palavras
- caracteres

## 5 — Reconhecimento de caracteres

Aqui acontece o OCR de verdade.

Modelos usados:

### Métodos antigos

- Template matching
- SVM
- HOG features

### Métodos modernos

Deep Learning:

- CNN
- LSTM
- Transformers

Modelos comuns:

CRNN (CNN + RNN)

Fluxo típico:

imagem → CNN → features → RNN → sequência de caracteres

##  Pós-processamento

Corrige erros usando:

- dicionários
- language models
- heurísticas

# . Tipos de OCR

## OCR simples

Reconhece caracteres isolados.
Exemplo:A  B  C

## OCR contextual

Reconhece **palavras e frases completas**.
Usa modelos linguísticos para prever:

"0LA MUND0" → "OLA MUNDO"

## OCR estrutural (document understanding)

Além de ler texto, entende **estrutura do documento**:

- tabelas
- campos
- recibos
- formulários

Exemplo:

Total: 45.90

vira
```json
{  
  "total": 45.90  
}
```

Ferramentas:

- Google Document AI
- Amazon Textract


[[google ml kit/ tesseract]]  