O nome _You Only Look Once_ vem da ideia principal do algoritmo:

> A rede neural olha para a imagem **uma única vez** e já retorna todos os objetos detectados.

Isso é diferente de métodos antigos de visão computacional que funcionavam em **duas etapas**:

1. Encontrar possíveis regiões da imagem com objetos
    
2. Classificar cada região
    

Esses métodos eram chamados de **two-stage detectors**, como:

- Faster R-CNN
    
- Mask R-CNN
    

O YOLO pertence à categoria:

**One-stage detectors**

Ou seja:

Imagem → Rede Neural → Objetos detectados

Tudo em um único passo.


# 2. O que o YOLOv8 consegue fazer

O YOLOv8 não serve apenas para detectar objetos. Ele suporta várias tarefas de visão computacional.

### 1️⃣ Detecção de objetos

Identifica objetos e cria **bounding boxes**.

Exemplo:

Pessoa → caixa delimitadora  
Carro → caixa delimitadora  
Cachorro → caixa delimitadora

Saída típica:

Objeto: pessoa  
Confiança: 0.92  
Bounding box: (x1,y1,x2,y2)

---

### 2️⃣ Segmentação de instância

Além da caixa, o modelo identifica **o formato exato do objeto**.

Exemplo:

- silhueta de pessoa
    
- contorno de um carro
    

Isso é útil para:

- edição de imagem
    
- robótica
    
- realidade aumentada
    

---

### 3️⃣ Pose estimation (detecção de esqueletos)

Detecta **pontos do corpo humano**.

Exemplo:

- cabeça
    
- ombros
    
- cotovelos
    
- joelhos
    

Usado em:

- análise esportiva
    
- reconhecimento de gestos
    
- fisioterapia
    

---

### 4️⃣ Classificação de imagens

Também pode funcionar como classificador simples.

Imagem → classe

Exemplo:

gato  
cachorro  
carro