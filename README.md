# Классификатор MNIST на базе LeNet-5 (PyTorch)

Реализация классической сверточной нейросети LeNet-5 в PyTorch для распознавания рукописных цифр из набора данных MNIST.

## 🧠 Модель

LeNet-5 — это сверточная нейронная сеть, изначально разработанная для задачи распознавания цифр. Архитектура модели в этом проекте:

- `Conv2D(1 → 6, ядро 5x5)` → ReLU → MaxPool
- `Conv2D(6 → 16, ядро 5x5)` → ReLU → MaxPool
- Преобразование в вектор → `Linear(400 → 120)` → ReLU
- `Linear(120 → 84)` → ReLU
- `Linear(84 → 10)` → выход (логиты по классам 0–9)

Размер входных изображений — **32×32**, как в оригинальной статье.

## 🗃 Датасет

Используется стандартный датасет [MNIST](http://yann.lecun.com/exdb/mnist/) (60 000 обучающих и 10 000 тестовых изображений).
