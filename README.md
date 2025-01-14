![Design sem nome(1)](https://github.com/user-attachments/assets/b378d269-5e78-4919-81e1-a0221bcb89e1)

# Desenho de Coração com Turtle

Este projeto utiliza o módulo `turtle` integrado ao Python para desenhar uma forma de coração na tela, plotando equações matemáticas para a curva do coração.

## Descrição
O programa:
1. Define duas funções matemáticas (`hearta` e `heartb`) que calculam as coordenadas x e y da forma de coração com base em um parâmetro `k`.
2. Usa o módulo `turtle` para plotar o coração, movendo-se para cada coordenada calculada.
3. Define a cor de fundo como preto e a cor do coração como vermelho para um apelo visual.
4. Desenha o coração utilizando um loop que itera sobre um intervalo de valores para calcular os pontos ao longo da curva e conecta esses pontos de volta à origem, criando a forma do coração.

## Visão Geral do Código
Aqui está o código Python:

```python
import math
from turtle import *

def hearta(k):
    return 15 * math.sin(k)**3

def heartb(k):
    return 12 * math.cos(k) - 5 * \
           math.cos(2 * k) - 2 * \
           math.cos(3 * k) - \
           math.cos(4 * k)

speed(0)  # Velocidade máxima de desenho
bgcolor("black")
color("red")

for i in range(0, 3000, 2):  # Desenha a curva do coração
    goto(hearta(i) * 20, heartb(i) * 20)
    goto(0, 0)  # Conecta de volta à origem

done()  # Finaliza o desenho
```

## Como Funciona
- **Funções Matemáticas**:
  - `hearta(k)`: Calcula a coordenada x com base no seno de `k`.
  - `heartb(k)`: Calcula a coordenada y usando uma combinação de termos de cosseno.
- **Comandos do Turtle**:
  - `goto(x, y)`: Move a tartaruga para a posição `(x, y)` especificada.
  - `speed(0)`: Define a tartaruga para a velocidade máxima.
  - `bgcolor("black")`: Altera a cor de fundo para preto.
  - `color("red")`: Define a cor do desenho como vermelho.
  - `done()`: Encerra o desenho.

## Saída
O programa produz uma forma de coração vermelha desenhada em um fundo preto, plotada matematicamente para precisão e apelo visual.

## Requisitos
- Python 3.x
- Módulo Turtle (já instalado com o Python)

## Executando o Programa
1. Salve o código em um arquivo, por exemplo, `desenho_coracao.py`.
2. Execute o programa:
   ```bash
   python desenho_coracao.py
   ```
3. Uma janela será aberta exibindo o coração sendo desenhado.

Aproveite o seu coração matematicamente preciso! ❤️
