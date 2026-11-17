# Machine_L2 — PandaPickCube RL Experiments

Практическая работа №2.
Обучение роботизированного манипулятора Franka Panda
в среде PandaPickCube с использованием алгоритма PPO.

## Эксперименты

| Эксперимент | Изменённый параметр | Success Rate |
|---|---|---|
| Baseline | Стандартная конфигурация | 90% |
| Num Envs 256 | num_envs = 256 | 0% |
| Box Target Strong | box_target = 40.0 | 0% |
| Qpos Strong | robot_target_qpos = 30.0 | 0% |
| Box Target 4 | box_target = 4.0 | 100% |

## Условия

- Среда: PandaPickCube
- Алгоритм: PPO
- Итерации: 1001
- Seed обучения: 1
- Тестирование: 10 эпизодов, seed = 42
- GPU: NVIDIA Tesla T4

## Содержимое

- train.py — исходный скрипт обучения
- train_experiments.ipynb — рабочий ноутбук экспериментов
- inference.py — скрипт тестирования
- results/ — модели, видео, логи TensorBoard и результаты тестирования

## Вывод

В проведённых испытаниях наибольшую успешность
показала модель Box Target 4: 10 успешных эпизодов из 10.
