# Описание задачи

Одним из классов объектов, встречающихся на спутниковых снимках, являются водоёмы. Сегментация водоемов имеет применение для автоматического создания топографических карт, мониторинга состояния водоемов, а также для оценки воздействия человеческой деятельности на водные экосистемы.

Для решения задачи сегментации воды вам будет предоставлен набор данных, включающий фрагменты спутникового снимка г. Екатеринбурга. Ваша цель - разработать алгоритм сегментации, который автоматически определяет области, соответствующие водным объектам на этих изображениях.

Особенностью этой задачи является то, что для целевого набора у участников не будет разметки. Вам предстоит обучить модель на общедоступных данных и обеспечить, чтобы ваша модель хорошо работала на тестовом наборе.

Модель должна быть способна выдавать маску по спутниковому изображению - матрица той же размерности, каждое значение которой определяет принадлежность пикселя либо к классу воды (=1), либо к фону (=0).

Самыми популярными подходами для решения задачи выделения воды на спутниковых снимков являются водные индексы и сверточные нейронные сети. Водный индекс — это число, полученное арифметическими операциями из значений каналов пикселя. Вычисление водного индекса — это очень быстрая и простая операция, однако основной недостаток водных индексов заключается в том, что это пороговый алгоритм. То есть необходимо подбирать значения порога вручную для каждого нового снимка, поскольку гистограмма снимка меняется в зависимости от спутника, времени съемки, метеорологических условий. Также водные индексы дают ложные срабатывания на тенях от зданий, плохо работают, если на воде есть рябь.

Сверточные нейронные сети являются более продвинутым алгоритмом сегментации, однако качество их работы и обобщающая способность напрямую связаны с качеством и составом обучающего набора, его разнообразием, так как сети обучаются на конкретных примерах.

Задача и данные предоставлены Институтом математики и механики имени Н. Н. Красовского УрО РАН.

*Kaggle notebook*: https://www.kaggle.com/code/l1ghtsource/rucode-4