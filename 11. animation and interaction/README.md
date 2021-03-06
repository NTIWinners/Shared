[Ссылка](https://www.khanacademy.org/computing/computer-programming/programming) на курс

1. `Parting Clouds`

   1. В этой задаче вам надо использовать свои магические возможности программиста, чтобы сначала создать пасмурное небо, а затем анимировать его в яркое и солнечное. Начните с изменения положения облаков так, чтобы они частично перекрывали солнце

      `Подсказка`: попробуйте изменить значения переменных `leftX` и `rightX`

   2. Теперь облака прячут солнце, и мы хотим анимировать их, чтобы они двигались в разные стороны от него. Сделайте так, чтобы левое облако перемещается на 1 пиксель влево в каждом кадре, а правое облако перемещается на 1 пиксель вправо. Помните, что вы можете нажать `Restart`, чтобы перезапустить свою программу.

      `Подсказка`: Для изменения `leftX` и `rightX` используйте инкременты и декременты, которые мы обсудили в последних двух примерах ([первый](https://www.khanacademy.org/computing/computer-programming/programming/animation-basics/p/incrementing-shortcuts), [второй](https://www.khanacademy.org/computing/computer-programming/programming/animation-basics/p/a-shorter-shortcut))

   3. Давайте сделаем так, чтобы облака разбегались от солнца, которое становится все больше и больше! Увеличивайте радиус солнца на 2 пикселя в каждом кадре.

2. `Shooting star`. Теперь, когда вы познакомились с основами анимации с помощью переменных, заставим упасть звезду! У вас уже есть код, объявляющий две переменные и рисующий звезду. Выполните шаги ниже, чтобы оживить звезду

   1. Решите, в какой части холста начнет движение ваша звезда. Измените начальные значения координат
   2. Решите, в каком направлении должна двигаться звезда. Изменяйте переменные внутри `draw` так, чтобы звезда двигалась так, как вы хотите.
   3. Добавить вторую звезду или другую фигуру и сделайте, чтобы она перемещалась в другом направлении.
   4. `Бонусное задание`: Измените форму звезды или траекторию движения (напимер так, словно объектом стреляют из пушки).
   5. `Бонусное задание`: Нарисовать на фоне звездную ночь или небоскребы.

3. \* Создайте машинку, движущуюся на зрителя

   <details><summary>Пример</summary>

   ![car](https://media.giphy.com/media/3o7WIOcNjgPc9uYs4U/giphy.gif)

   </details>

4. \* Приведенный код рисует точку двужущуюся [по синусоиде](https://ru.wikipedia.org/wiki/Синусоида), используя функцию `sin()`. Добавь еще хотя бы 3 точки и настрой движение так, чтобы анимация стала напоминать ползущую змею

   <details><summary>Заготовка кода</summary>

   ```javascript
   var x = 0;
   var y = 50 * sin(x / 50) + 200;

   function setup() {
       createCanvas(400, 400);
       noStroke();
   }

   function draw() {
       background(48, 48, 48);
       ellipse(x, y, 20, 20);

       x = x + 1;
       y = 50 * sin(x / 50) + 200;
   }
   ```

   </details>

   <details><summary>Пример</summary>

   ![snake](https://media.giphy.com/media/xUOwG4Tqfc07UOcLYY/giphy.gif)

   </details>

5. `Tasty Tomato`

   1. Давайте внесем небольшие изменения перед тем, как мы научим программу взаимодействовать с мышью. Видите следы укуса на помидоре? Сейчас укус слишком маленький, сделайте его больше!

      `Подсказка`: укус отрисовывается как эллипс. Чтобы сделать его больше, поменяйте ширину и высоту эллипса на значение не меньшее, чем 60.

   2. Теперь у нас есть ровно один укус на помидоре - но мы-то хотим съесть его весь! Мы можем сделать это, рисуя новый укус каждый раз, когда пользователь сдвигает мышь. Первый шаг - создать функцию `draw()` и перенести код, рисующий укус, в нее.

      `Напоминание`: перенести код *в* функцию - или поместить *внутри* функции - означает расположить код между {фигурными скобками}, которые находятся после функции.

      `Подсказка`: Вы можете выделить и перетащить мышью участок кода, чтобы передвинуть его.

   3. Осталось сделать так, чтобы появлялись новые укусы, когда мы двигаем мышью. Для этого необходимо изменять координаты `x` и `y` укуса, основываясь на `mouseX` и `mouseY`. Чтобы удостовериться, что все работает, просто води мышью!

6. `Mouse movement mania`

   1. Эта программа рисует разноцветные фигуры на экране, когда пользователь двигает мышью, но мы собираемся поменять это! Первым делом измени вызов функции `fill()` так, чтобы круги становились разных цветов. Помни, что ты можешь использовать `mouseX` и `mouseY` как параметры, чтобы создать разнообразие цветов.
   2. Теперь измени по своему вкусу вызов `ellipse()`. Ты можешь изменить размер эллипсов или изменять их форму, используя `mouseX` и `mouseY` как параметры.
   3. Добавь цвет обводки эллипса. Убери вызов `noStroke()` и вызывай `stroke()` внутри функции `draw()`

7. \* `Прикленная машинка`

   1. Нарисуйте машинку и сделайте так, чтобы она следовала за движением мыши по горизонтали

   2. Измените движение машинки так, чтобы она была не намертво приклеена к положению курсора, а плавно подъезжала к нему.

      `Подсказка`: Следует вычислять разницу между координатой мыши и прошлым положением машинки

      ![](https://api.monosnap.com/rpc/file/download?id=CugYO7tBOmqpcQWTotHd9KsepBmqLS)

8. `Quiz: Variable Expressions`

   1. Эта программа рисует прямоугольник, используя переменные `w` (для ширины) и `h` (для высоты)

      ```javascript
      var w = 10;
      var h = 50;
      rect(200, 200, w, h);
      ```

      Пусть `h` зависит от `w` так, что если мы изменим значение `w`, то `h` изменится пропорционально так, что `h` всегда в 5 раз больше, чем `w`. Тогда какое выражение должно храниться в `h`?

   2. Пусть у нас есть программа, которая рисует мороженое (треугольник) с двумя шариками мороженого (два эллипса) сверху. Второй шарик чуть меньше первого и у нас есть 2 переменные, `scoop1` и `scoop2`, в которых хранятся размеры шариков:

      ```javascript
      var scoop1 = 40;
      var scoop2 = 30;
      triangle(200, 250, 180, 200, 220, 200);
      ellipse(200, 180, scoop1, scoop1);
      ellipse(200, 145, scoop2, scoop2);
      ```

      Если  мы хотим сделать `scoop2` зависящим от `scoop1` так, чтобы `scoop2` был всегда на 10 пикселей меньше, чем `scoop1`, какое выражение должно храниться в переменной `scoop2`?

   3. Следующая программа рисует 2 прямоугольника: большой и маленький. Переменные `big` и `small` хранят размеры этих прямоугольников:

      ```javascript
      var big = 100;
      var small = 10;
      rect(100, 100, big, big);
      rect(100, 100, small, small);
      ```

      Мы хотим сделать `small` зависящим от `big` так, чтобы они сохраняли ту же пропорцию, когда мы меняем их -  `small` должен быть всегда равен 1/10 размера `big`. Какое выражение должно храниться в `small`?

   4. Пусть у нас есть программа, которая рисует лицо и тело с помощью эллипсов. Она использует 2 переменные, одну для размера тела и вторую для размера лица:

      ```javascript
      var bodySize = 100;
      var faceSize = 50;
      ellipse(200, 200, bodySize, bodySize);
      ellipse(200, 150, faceSize, faceSize);
      ```

      Если  мы хотим сделать `faceSize` зависящим от `bodySize` так, чтобы `faceSize` был всегда равен половине `bodySize`, какое выражение должно храниться в `faceSize`?

   5. В этой программе значение `b` зависит от значения `a`, а значение `c` зависит от значения `b`. Функция `println()` выводит в консоль результат вычисления переданного ей выражения:

      ```javascript
      var a = 25;
      var b = a / 5;
      var c = b + 30;
      println(b + c);
      ```

      Что эта программа выведет в консоль?

   6. Следующая программа рисует 2 прямоугольника, где переменные `width1` и `width2` хранят их ширину. При этом `width2` зависит от `width1`:

      ```javascript
      var width1 = 12;
      var width2 = 2 * width1 + 5;
      rect(50, 50, width1, 10);
      rect(50, 80, width2, 10);
      ```

      Если мы заменим начальное значение `width1` на 6, какое числовое значение выражения будет храниться в `width2`?

9. `Brown bear eyes`

   1. В этом задании мы на примере этого мишки потренеруемся в масштабировании с помощью дробей и переменных

      Попробуй изменить значения `x` и `y`. Заметь, что уши и нос двигаются вместе с мордой, но глаза не двигаются

      Попробуй изменить значение `faceSize`. Заметь, что размеры ушей и носа меняются вместе с размерами морды, но размеры глаз не меняются.

   2. На этом шаге ты улучшишь код так, что размер глаз будет изменяться вместе с изменением размеров морды.

      Если ты посмотришь на выражения, рисующие глаза, то заметишь, что ширина и высота (третий и четвертый параметры) пока равны 20. Изначально, до того ты как изменил его, `faceSize` был равен 160. Таким образом, чтобы сохранить изначальные пропорции, глаза должны всегда быть равны 20/160 или 1/8 от размеров морды.

      Чтобы глаза всегда были равны 1/8 размеров морды, сделай следующее:

      - Создай новую переменную для хранения размера глаз и  присвой ей `faceSize/8`
      - Замени значение 20 в эллипсах, рисующих глаза, на имя этой переменной

   3. Теперь при изменении `x` морда движется влево или вправо, но глаза остаются на месте.  На этом шаге ты исправишь код так, что когда морда движется влево или вправо, левый глаз будет двигаться синхронно. (Мы исправим правый глаз на следующем шаге)

      Если ты посмотришь на выражение, рисующее левый глаз, то заметишь, что координата x (первый параметр) равна 160. Изначально, до того ты как изменил их, `x` был равен 200, а `faceSize` был равен 160. Таким образом, чтобы сохранить изначальный промежуток между левым глазом и центром морды, координата x левого глаза должна быть на `(200 - 160) / 160` или `1/4` от размера морды левее `x`.

      Чтобы глаза всегда находились на `1/4` размера морды левее `x`, сделай следующее:

      - В эллипсе, рисующем левый глаз, замени значение 160 на `x - faceSize / 4`

   4. Теперь при изменении `x` морда движется влево или вправо, но правый глаз остается на месте.  На этом шаге ты исправишь код так, что когда морда движется влево или вправо, правый глаз будет двигаться синхронно

      Если ты посмотришь на выражение, рисующее правый глаз, то заметишь, что координата x (первый параметр) равна 240. Изначально, до того ты как изменил их, `x` был равен 200, а `faceSize` был равен 160. Таким образом, чтобы сохранить изначальный промежуток между правым глазом и центром морды, координата x левого глаза должна быть на `(240 - 200) / 160` или `1/4` от размера морды правее `x`.

      Чтобы глаза всегда находились на `1/4` размера морды правее `x`, сделай следующее:

      - В эллипсе, рисующем правый глаз, замени значение 240 на `x + faceSize / 4`

   5. Теперь при изменении `y` морда движется вверх или вниз, но глаза остаются на месте.  На этом шаге ты исправишь код так, что когда морда движется вверх или вниз, глаза будут двигаться синхронно

      Если ты посмотришь на выражение, рисующее глаза, то заметишь, что координата y (второй параметр) равна 180 для обоих из них. Изначально, до того ты как изменил их, `y` был равен 200, а `faceSize` был равен 160. Таким образом, чтобы сохранить изначальный промежуток по вертикали между глазами и центром морды, координата y глаз должна быть на `(200 - 180) / 160` или `1/8` от размера морды выше `y`.

      Чтобы глаза всегда находились на `1/8` размера морды выше `y`, сделай следующее:

      - В эллипсе, рисующем правый глаз, замени значение 180 на `y - faceSize / 8`

   6. Теперь, когда мы выполнили всю тяжелую работы, ты можешь понастраивать `x`, `y` и `faceSize`.

      Чтобы проверить, что твои исправления работают, подвинь мишку в левый нижний угол и сделай медведя действительно большим (сделай `x < 150`, `y > 250`, `faceSize > 350`)!
