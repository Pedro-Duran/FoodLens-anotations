Pesquisando sobre o [[Yolo]], destrinchei subtópicos de aprodundamento que acredito que possam ser interessantes para nos aprofundarmos: 

# 1   métodos de visão computacional
notei que tenho que ler sobre [[Two stage detectors]], o modelo utilizado no nosso projeto é o Yolov8, que é um [[one stage detector]] , seus predecessores (v7 e v5) eram two stage detectors.

# 2 Outputs
No tópico 2 da nota [[Yolo]], conseguimos vislumbrar um exemplo de output, nele é mencionado a confiança que o modelo tem na acurácia de sua identificação. 

```json 
Objeto: pessoa  
Confiança: 0.92  
Bounding box: (x1,y1,x2,y2)
```
- [ ] É interessante pensar em boas práticas no mercado no que toca a precisão da informação, não lembro se foi Pedro ou Davi quem mencionou o seguinte:
 Uma vez que o Yolo detecta o nome do produto, também podemos fazer uma segunda etapa de verificação usando um modelo [[OCR (Optical Character Recognition)]] 
 - [ ] Identificar qual ferramenta utilizar, ML Kit ou Tesseract. Acredito que pelo que foi destrinchado no [[ tesseract]], já dá pra gente fazer uma escolha
 - [ ] 
 .   É interessante comparar nossa lógica (nosso primeiro pensamento quando diante da questão "como lidar com a precisão da informação?") com as soluções encontradas pelas gigantes do mercado. Acho que seria legal pesquisar algumas empresas (como spotify, netflix, uber, todas essas que tem techBlog) e como elas fazem para otimizar a acurácia dos seus modelos de IA. 

# 3 uma arquitetura baseada em **CSPDarknet modificada**.


Uma rede YOLO geralmente tem três partes principais:

Backbone, Neck e head.

Com o input sendo a imagem e o Ouput sendo as detecções,
o que cada uma das partes faz:

### Backbone

Extrai **features da imagem**.

Exemplo: bordas, texturas, padrões
    

### Neck

Combina informações de diferentes escalas da imagem.

Isso permite detectar se objetos são  grandes ou pequenos.
    
- [[FPN (Feature Pyramid Network)]]
    
- [ ] [[PAN (Path Aggregation Network)]] 

### Head

A head é responsável por gerar as previsões:
Para cada objeto:
```json
classe  
bounding box  
confiança
```

YOLOv8 utiliza [[anchor-free detection]], diferente das versões antigas. 

# 4 tipos de modelo YOLOv8 

Aqui acho que seria interessante fazermos uma análise com parâmetros a nível de processamento computacional, mesmo:

Existem diferentes tamanhos de modelo.

|Modelo|Uso|
|---|---|
|YOLOv8n|nano (muito rápido)|
|YOLOv8s|small|
|YOLOv8m|medium|
|YOLOv8l|large|
|YOLOv8x|extra large|

Comparação:

|Modelo|Velocidade|Precisão|
|---|---|---|
|nano|muito rápido|menor|
|small|rápido|boa|
|medium|equilibrado|melhor|
|large|mais pesado|alta|
|xlarge|pesado|máxima|
# Aplicações reais

YOLOv8 é amplamente usado em:
### Segurança
- reconhecimento de pessoas
- detecção de armas
- vigilância
### Veículos autônomos
- detectar carros
- pedestres 
- sinais
### Agricultura
- contagem de plantas
- identificação de pragas
### Medicina
- detecção de tumores
- análise de imagens médicas
### E-commerce
- reconhecimento de produtos
- inventário automático
Seria interessante saber explicar exatamente como direcionar o yolo a reconhecer um tumor ou uma arma. 

# 5 - Por que o YOLO é tão rápido?
### 1️⃣ Apenas uma passagem pela rede

Imagem → rede → resultado

### 2️⃣ Predição paralela

A imagem é dividida em **grid cells**.

Cada célula prevê:
```json
objetos  
classes  
caixas
```

### 3️⃣ Otimização para GPU

YOLO foi projetado para rodar em:

- GPU, edge devices, tempo real
Pode chegar a 60 FPS

#  Limitações

### 1️⃣ Objetos muito pequenos

Podem ser difíceis de detectar.
### 2️⃣ Oclusão

Objetos parcialmente escondidos podem gerar erros.

### 3️⃣ Dependência do dataset

A qualidade depende muito de:

- anotações e diversidade do dataset

