O **Tesseract** é um dos motores de OCR mais conhecidos do mundo.

Originalmente desenvolvido pela **HP** e depois mantido pelo:

- Google
Repositório:
- [https://github.com/tesseract-ocr/tesseract](https://github.com/tesseract-ocr/tesseract)

## Características

- open source
- suporta mais de **100 idiomas**
- funciona offline
- altamente configurável


---

## Arquitetura moderna (Tesseract 4+)

A partir da versão 4 ele usa **deep learning**:

`LSTM-based OCR engine` 

Pipeline simplificado:
`
```
imagem  
↓  
detecção de linhas  
↓  
rede LSTM  
↓  
sequência de caracteres
```

O **Google ML Kit** é um SDK de **machine learning para apps mobile**.

Ele oferece vários recursos:

- OCR (Text Recognition)
- face detection
- barcode scanning
- object detection

Desenvolvido pela:

- Google

## OCR no ML Kit

O ML Kit possui um módulo chamado:
Text Recognition

Ele funciona **diretamente no dispositivo (on-device)**.

```
Fluxo:

câmera  
↓  
detecção de texto  
↓  
OCR  
↓  
retorno estruturado
```

## Estrutura retornada

ML Kit não retorna apenas texto.

Ele retorna estrutura:

Text  
 ├── TextBlock  
 │     ├── Line  
 │     │     ├── Element


Isso facilita:

- leitura de recibos
- leitura de placas
- leitura de cartões
## Vantagens

✔ rápido  
✔ funciona offline  
✔ otimizado para mobile  
✔ fácil de integrar
## Desvantagens

❌ menos configurável  
❌ não open source  
❌ menos controle do modelo
# 6. Comparação: Tesseract vs ML Kit

| Característica     | Tesseract         | ML Kit      |
| ------------------ | ----------------- | ----------- |
| Tipo               | Biblioteca OCR    | SDK ML      |
| Plataforma         | Desktop / backend | Mobile      |
| Offline            | Sim               | Sim         |
| Open source        | Sim               | Não         |
| Configurável       | Muito             | Pouco       |
| Estrutura de texto | Limitada          | Boa         |
| Facilidade         | Média             | Muito fácil |

# 7. Outras ferramentas modernas de OCR

EasyOCR
PaddleOCR
Google Vision API
Amazon Textract

# 8. Exemplos de aplicações reais

OCR é usado em:
### Fintech
- leitura de boletos
- leitura de documentos
### Logística

- leitura de placas
- leitura de etiquetas

### Apps mobile

- digitalização de cartões
- tradução em tempo real

### Arquivamento

- digitalização de livros

---

# 10. Onde OCR aparece em IA moderna

Hoje OCR está integrado com:
### Vision Transformers

modelos multimodais que entendem:

imagem + texto

Exemplo:

- GPT-4V
- Donut
- LayoutLM

Eles fazem:

document understanding



✅ **Resumo**

OCR transforma texto presente em imagens em texto digital usando visão computacional e machine learning.

Ferramentas principais:

|Ferramenta|Uso|
|---|---|
|Tesseract|OCR open source para backend|
|ML Kit|OCR para apps mobile|
|EasyOCR|OCR deep learning em Python|
|PaddleOCR|OCR avançado moderno|
|Google Vision|OCR cloud|