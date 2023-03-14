# Вор РПГ 2
### Бот работает первые 15 минут каждого часа(за исключением голосовых)
### Все награды использованные когда бот находится офлайн будут приняты сразу после его запуска

## Суть

1. Копим баллы канала.
2. Переводим баллы в души(внутренняя валюта бота) с помощью следующих наград:
    * Для малоимущих - Курс:1к0.9 Вероятность успеха 100%
    * Для Шейхов - Курс:1к1 Вероятность успеха 100%
    * Для Лудоманов - Курс:1к2 Вероятность успеха зависит от удачи
    
4. С помощью душ качаем характеристики персонажа.
5. Дуэлимся, чтобы получить ещё больше душ.
6. Способы получить випку:
   * С помощью `!steal` воруем випку у случайного випа, в случае проигрыша бан на 24 часа, и вип получает 16666 душ .
   * Воровство эта та же самая дуэль, только на кону випка или бан(Возможно в будущем это изменится, посмотрим как пройдет бета)
   * Випку можно купить с помощью команды `!buy`. Випка может купиться или нет(Вероятность зависит от количества випов на канале, чем больше, тем меньше)

## Характеристики
* **HP**(Здоровье)
* **STR**(Сила)
* **DEX**(Ловкость)
* **ARC**(Удача)

## Команды
`!time` - время до запуска бота

`!levelup HP,STR,DEX,ARC amount` - увеличивает выбранную характеристику на amount 

`!stats` - показывает ваши характеристики

`!stats username` - показывает характеристики username

`!duel` - Вы встаёте в поиск дуэли, следующий человек который введет `!duel` вступит с вами в дуэль. (Для использования необходимо иметь не менее 2000 душ)

`!steal` - (Стоимость 50000) Попытка украсть випку. Вы вызываете на дуэль случайного випа.
В случае победы вы получите випку. В случае проигрыша вы отправитесь в бан на 24 часа, а вип получит 16666 душ

`!buy` - (Стоимость 350000) Попытка купить випку.(Шанс успеха зависит от количества випов на канале 50% если 50 випов. 10% если 90 випов)

`!give_vip username` - отдаёт вашу випку username


`!play name` - `Стримлер пока не настроил, но завтра точно-точно настроит` 
![CoolStoryBob](https://static-cdn.jtvnw.net/emoticons/v2/123171/default/dark/1.0)
воспроизводит звуковую команду за души. Название, стоимость и кулдауны звуковых команд смотрите в файле звуковые.csv

## Дуэли
Дуэли пошаговые

### Ход дуэли:
1. Характеристики умножаются на коэффициент удачи.(Зависит от отношения удачи участников)
2. Выбирается, кто ходит первым.(Шанс зависит от отношения ловкости участников)
3. Поочередно происходит обмен атаками, пока здоровье одного из участников не станет меньше или равно 0
4. Есть 3 типа атак: Сильная(Базовый урон * 2), Нормальная(Базовый урон * 1), Слабая(Базовый урон * 0.5)
5. Базовый урон зависит от вашей Силы.
6. Вероятность типа атаки зависит от отношения ловкости участников.


Победитель забирает 80% душ проигравшего, но не больше 80% от ваших душ.

Пример 1: У вас 10000 душ, у противника 5000. Вы выиграли и получите 4000

Пример 2: У вас 5000 душ, у противника 10000. Вы выиграли, и получите 4000
