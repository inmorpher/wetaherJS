Доброго времени суток!

Сразу оговорючь что прошел только 13 уроков и завис на этом проэкте, уж очень он меня зацепил.
Усложнил себе задачу максимально. Верстка минимальная, я хотел что бы элементы создавались.
В полне возможно по неопытности мог использовать где-то костыли, а где-то можно было упростить/оптимизировать.
Разобрался с колекциями и NODE-листами

немноечко хочу пояснить что было наделано.

1. Был сделан переключатель тем. Так как не смог определиться какая цветовая схема мне больше нравиться.

2. Функция cardFeelUp создает и наполняет главнный блок с погодой на сейчас с первого запроса т.к. в бесплатном API 
    пока не до окнца реальизован one call api.

3. createMoreInfo клонирует и размножает блоки с погодой на 24 часа. Тут делаю изначальну проверку что если
    в родительском элементе есть уже блоки, то не создаем, а перезаполняем данные. В противном случае создаем и наполняем.

4. feelUpDayCard тут тот же принцип, нужно было только сделать оптимизированный цикл. В запросе на 5 дней с шагов в 3 часа
    есть не большая загвоздка. Я отсекал текущий день и завел каунтер для индикации что я нашел нужные мне жлементы и не более.
    Принцип в том что мы идем с шагов в 1 до того момента как текущий день отличается и время равно 03. с этого момента я прыгаю 
    в создании элесентов с шагом в 6, тогда выходит что я прыгаю по все индексам с временем 3 утра. в процессе обращаюсь на i + 3
    что дает мне время 15. Таким образом и наполняю ночь/день. Каунтер служит для отсекания последненго дня. Обьект который приходит 
    с сервервера имеет массив на 40 жлементов И 5 суток начинаются от Времени запроса. В этом слечае последний день мог быть не полным.

    в перенаполнении хожу с в 3 и использую коллекцию.

5. sunBlockFeelUp создает в 24-м блоке элементы рассвет/закат. Но было убрано для показа в первом и последннем элементе
    верстка плывет. Относительно для меня было сделано сложное условие для правильности их вставки.
    sunBlockReBuild удаляет элементы и переставлыет из местами т.к. время рассвета и закаат в разных странах рахное.

6. getDayStatus, getMonth, getWindInfo, getTime чисто функции для обработки значений вертра, времени, месяца.

Пы Сы. Знаю что можно было тупо все сверстать и наполнять. Вышло бы в два раза меньше работы, но такую цель перед собой не ставил
        хотел проверить собтвенные сили. Что же буду учить дальше, в дальнейшем возьму у вас курс по ПХП.
        Долго сомнивался ПХП или Нода. Посмотрев на регулярные хостинги и в большинстве нолда только под VPS. Думаю в моем сечае выбор очевиден.

        Спасибо за ваши курсы. Действительно очень позновательно !! так держать!

        телеграм @inmo_0

        omennnn62@gmail.com