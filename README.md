# chizou-asp-msu

## Численные методы решения задач оптимального управления

1. `shooting_method.py`. 
Решаем задачу вида $$ J =\int^{0}_{1} f_0(t, x(t), u(t)) -> min $$

Рассмотрим функционал $$ J =\int^{0}_{1} (x(t)+1)^{2} -> min $$
    
$$ f_0(t,x,u) = (x(t) - 1)^2 $$

$$ x(t) - u(t) = 0,  \forall t \in [0,1] $$

$$ u(t) \in R^1(-\infty, +\infty), \forall t \in [0,1] $$
    
$$ x(0) - 1 = 0 $$
$$ x(1) - 1 = 0 $$

Ограничения типа неравенств отсуствуют.

Для поиска оптимального решения используем пакет `Gekko` с испльзованием встроенного 
алгоритма уточнения решения методом стрельбы (shooting method)

```bash
pip install gekko flask flask-cors
```

