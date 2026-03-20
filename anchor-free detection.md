# Anchor-free detection (uma grande mudança)

Modelos YOLO antigos usavam **anchors**.

Anchors são caixas pré-definidas:
```json
pequena  
média  
grande
```

O modelo ajustava essas caixas.

Problemas:

- precisa calibrar anchors    
- menos flexível

YOLOv8 usa abordagem **anchor-free**, onde a rede prevê diretamente:
```json
centro do objeto  
largura  
altura
```

Isso melhora:

- precisão
- simplicidade