TODO:
9) проверить все валидационные выборки (чтобы было поровну HC & ALS)

10) сделать 4 сверточных слоя на каждом диапазоне
11) use lightening framework (future)

CHANGE-LOG

1) best model on each fold selection using validation set criterion
2) Estimate performance using this best model
3) create 3-row conv NN architecture: low-freq, mid-freq, high-freq
4) Add batch normalization layer
5) wider time span works better (!) -- experiment with this
6) accelerate test and validation process
7) added second layer of convolutions

## Анализ проблемной вкалдки (номер 3)

В результате экспериментов замечено, что результат тестирования при обучении на вкладке 3 всегда очень низкий. Не более 60%. Нужно понять с чем это связано?

Номера дикторов из этой вкладки
[61->HC(f),
 16->HC(m),
 115->HC(f),
 109->HC(f),
 111->HC(f),
 2->HC(f),
 107->HC(m),
 46->ALS(f),
 84->ALS(m),
 64->ALS(m),
 52->ALS(f),
 24->ALS(m),
 76->ALS(m)
 ], # 2+5 HC / 4+2 ALS

Номера валидационной выборки для этой вкладки
 [28->HC(m), 99->HC(f), 129->HC(f), 55->ALS(m)],
