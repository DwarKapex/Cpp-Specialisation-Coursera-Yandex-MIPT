Необходимо добавить к home desktop version поддержку нового запроса:

1. Spend from to value: потратить указанную сумму равномерно за указанный диапазон дат. Теперь чистая прибыль в запросах ComputeIncome вычисляется как разница заработанного (за вычетом налогов) и потраченного. При расчёте налога потраченные суммы не учитываются.

Кроме того, в запросах PayTax теперь нужно принимать процент, который нужно заплатить:

1. PayTax from to percentage: заплатить указанный налог в указанный диапазон. Гарантируется, что percentage — целое число от 0 до 100.

# Пример

Ввод

```
8
Earn 2000-01-02 2000-01-06 20
ComputeIncome 2000-01-01 2001-01-01
PayTax 2000-01-02 2000-01-03 13
ComputeIncome 2000-01-01 2001-01-01
Spend 2000-12-30 2001-01-02 14
ComputeIncome 2000-01-01 2001-01-01
PayTax 2000-12-30 2000-12-30 13
ComputeIncome 2000-01-01 2001-01-01
```

# Вывод

```
20
18.96
8.46
8.46
```