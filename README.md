# МЛиТА экзамен (вопросы и ответы)

***1) Как доказать общезначимость формулы без кванторов?***

**Ответ:**
1) *Определение (из введений Гордеева):* Формула логики предикатов называется **логически общезначимой**, если она истинна в любой интерпретации.
(Простым языком: Логическая общезначимость формулы означает, что какую бы ни выбирали область интерпретации и какие бы соответствия не задавали, мы всегда будем получать истинные отношения или высказывания)

2) Построим таблицу, в которой A и B - предикаты, F - конечная данная формула. Предполагаем, что в какой-то интерпретации каждая из формул A и B - истинна или ложна. Если конечная формула F - истинна при любых входях подформулах, то F - общезначима.

***2) Как переформулировать задачу в оптимизационной форме в задачу в форме распознавания хелпанитет? (Можно ли переформировать задачу в форме оптимизации в форму распознавания, и значит ли это что NP трудная задача переформулируется в NP полную?) (Как переформулировать задачу из формы оптимизации в форму распознавания? Следует ли из этого, что np-hard в форме оптимизации всегда можно переформулировать в npc в форме распознавания?)***

(Я привёл пример задачи комивояжера в двух формах (он принял), а про второй вопрос он сказал, что я ответил не на тот)
**Ответ:** На счёт оптимизации
можно поставить какие- нибудь пороги
типа если у тебя оптимизация перехходит порог - то есть, если не переходит, то нет
грубо говоря, нужно проверить 
есть ли а графе ГЦ
А у тебя задача по оптимизации: цикл опр длины
порогом будет - число вершин
попробуй так
Если непонятно - могу другими словами попытаться
А нельзя просто поменять вопрос «какой?» на «существует ли?»

***3) Как из нестрогого включения п в п поли получить строгое? (строгое включение P в P/Poly)***

(тема алгоритмически неразрешим задач)

**Ответ:** сказать о существовании алгоритмически неразрешимых задач.
В вопросе про строгое включение P в P/Poly он в основном говорит об алгоритмически неразрешимых задачах и их отношению к P/ Poly
Он хотел бы услышать про функцию натурального аргумента... (см. Стр 80 старого конспекта)


P/poly-мн-во предикатов таких, что набор функций, получаемые от этих предикатов, реализуются за полиномиальные схемы от n, где n-количество переменных в функции
P/poly - A(x1,x2...): f1(x1),f2(x1,x2) и тд реализуются за P(n), где A-предикаты
видимо как-то так
P(n)-полином

***4) V - Любой
Е - Существует
VxA(x) -> (Ex не C(x) -> Ex не (A(x) -> C(x)))
Исследовать на выполнимость и тд***

**Ответ:** не общезначима
UPD: кирпич сломался, формула общезначима и это доказано на семинаре
Определение сложности в худшем случае для НМТ и ОМТ

***5) VxEy A общезначима
ExVy A не выполнима
Сущестаует ли формула А для которой вот это верно?***

**Ответ:** да, существует. x~y(на булевых, к примеру и тд)/ x==y (более общий, вроде бы)/(или подобные). 

***6) Можно ли заменить в теореме Кука КНФ-выполнимость на тождественную ложь?
Проверьте ответ пожалуйста. Если NP=Co-NP, то можно.
Норм логика?***

**Ответ:** Теорема 9.2.  Если NP=Co-NP, то можно, тк первый аункт теоремы Кука - доказать, что задача принадлежит NP. Данная задача(с тождественной ложью) принадлежит coNp, отсюда и ответ, полученный выше.

***7) Можно ли дать определение ОМТ с помощью языка исчисления предикат ?***
(можно сделать (что-то в направлении функцию представить как предикат, можно использовать кванторы, существует два состояния, обратится в любой момент времени, это неверно, но направление правильно))

**Ответ:** Да, можно.  По сути, мы подаём на НМТ некий вход, условия, далее ОМТ что-то делает и даёт на выходе ответ. Рассуждения далее только для задач в форме распознования, где возможен бинарный ответ.
Пусть есть n+1 местный предикат, где n -длина входа, условия. На вход этого предиката подаётся оракульная функция, а также вход(в качестве n как раз термов).Далее предикат выдаёт 1, если ответ "да", и 0, если ответ "нет". Это учитывает возможность многократного вызова оракула. Внутри предиката как-то проверяется вход, обрабатывается, в том числе с вызовом оракула произвольное количество раз(в него можем подавать любой кусок входа, или весь вход).
(если он скажет, что память должна быть динамической, то омт -  это множестов предикатов, с одинаковыми свойствами, просто отличающиеся длинной входа)

Вариант 2: логика та же, только преликат 2местный, и один вход - оракульная функция, другой - вход, условие задачи.

***8) Теорема Ланднера***
(Саму теорему можно найти в старом конспекте, ctrl+F. Думаю, что её смысл - то, что класс NP неоднороден. Т.е. если P не равно np, то разбить np можно минимум на 3 класса: np-полные(npc), полиномиальные(p) и вот этот класс по середине, существование которого доказывается в этой теореме. Т.е. если есть задача из нп, и она не в нпс и не в п, то это не всегда значит, что просто не смогли доказать один из 2 фактов, возможно, она в 3 классе.) Только классов не три, а больше, ибо серединка эта неоднородна

**Ответ:** 
Эта теорема имеет практическое применение, если PNP. Пусть B – задача «Гамильтонов цикл», тогда теорема утверждает, что найдется такой класс распознаваемых за полиномиальное время графов, что на этом классе графов задача «Гамильтонов цикл», не имея полиномильного алгоритма решения, в то же время не является NP-полной.

Если P!=NP, то теорема утверждает непустоту NPI класса и дает
представление о его структуре. Он состоит из бесконечной совокупности
классов эквивалентности языков, каждый из которых «чуть-чуть» сложнее
другого. Кроме того в нем есть пары языков, ни один из которых
полиномиально не сводится к другому!
 
это про т ладнера из конспекта

![картиночка из лекций](https://github.com/Medvate/mlita_exam/blob/45/images/image.png)

***9) всегда ли в базисе кон диз отр наим сложность сфэ для функции - схаема реализации её мин днф
дайти опр классу п поле с имп языка исчисления предикатов***
(Нет, так как можно использовать КНФ. Зависит от количества 0 и 1 в таблице.)

**Ответ:** Точно нет. доказательство - примером. функция: НЕ(xy). сложность - 2
её мин днф: НЕ(х)\/НЕ(у), сложность - 3


***10) Определение сложности в худшем случае для НМТ и ОМТ***

(Дается через общее определение лсожности в худшем, накладывается на определения сложностей НМТ, ОМТ. В нмт - минимум по всез отгадам по данному условию. ОМТ - аналогично МТ, тк к оракулу за такт обращаемся)

**Ответ:** и новый, и старый конспекты.


***13) Теорема о соотношении МТ и НАМ
Мини вопрос: Может ли CoNP лежать в NP (да может, есть пересечение (класс P))***

**Ответ:**


***16) Как связана сложность МТ и количество команд в ней***

**Ответ:** никак. Сложность МТ связана с понятием "количество тактов работы". Команд может быть как больше, так и меньше,каждая команда может произвольное число тактов вызвать(хоть зациклить до бесконечности), поэтому никак.

***17) Пример сводимости по Тьюрингу***

**Ответ:**

***18) Почему PSPACE лежит в EXPTIME ?***

**Ответ:**

***20) Дать определение класса P/Poly при помощи исчисления предикатов? (Определить понятие P/Poly с использованием языка предикатов?)***

**Ответ:** 1) *Определение:* **P/poly** - множество предикатов таких, что набор функций, получаемые от этих предикатов, реализуется за полиномиальные схемы от n, где n - количество переменных в функции.

2) *Определение:* **P/poly** - множество предикатов вида P, таких, что функции f1, f2,..., fn,... реализуют СФЭ полиномиальной сложности по n. (Существует P - предикат, который определен на множестве всех двоичных последовательностей длины от 1 до бесконечности f1(x1)=P1, f2(x1,x2)=P2, ... fn(x1, ..., xn)=Pn,  Pn - это функция он n переменных.)

3) *Определение:* **P/poly** - A(x1,x2...): f1(x1),f2(x1,x2) и тд реализуются за P(n), где A-предикаты, P(n)-полином

4) *Определение (из введений Гордеева):* Класс булевых функций, для которых существуют схемы полиномиальной сложности обозначим через **P/poly**.

из лекции: 

![пполи через предикаты](https://github.com/Medvate/mlita_exam/blob/45/images/%D0%BF%D0%BF%D0%BE%D0%BB%D0%B8%20%D1%87%D0%B5%D1%80%D0%B5%D0%B7%20%D0%BF%D1%80%D0%B5%D0%B4%D0%B8%D0%BA%D0%B0%D1%82%D1%8B.png)

***21) Привести пример алгоритмически неразрешимой проблемы с доказательством.***

**Ответ:**  Теорема. Проблема остановки алгоритмически неразрешима.
Доказательство. От противного. Пусть такая машина T* существует. Тогда на входе (T,x) она выдает ответ «да», если машина Т останавливается на этом входе, и «нет» в противном случае. (Здесь Т – слово в алфавите А, являющееся описанием машины Т). Тогда по Т* можно построить машину Тьюринга T’(x), которая в случае, если T*(x,x)=”да”, начинает двигать головку в одну сторону и зацикливается, а в случае T*(x,x)=”нет” она останавливается. Что в этом случае будет означать T’(T’)? Остановится или нет машина на этом входе? Если «да», то это означает, что T*(T’)= «нет», т.е. T’ не должна останавливаться на T’. Если «нет», то это означает, что T*(T’)= «да», т.е. T’  должна останавливаться на T’.
Получили противоречие
Теорема доказана.


Рассмотрим функцию натурального аргумента f(n), принимающую значения 0 или 1. Можно показать, что вычисление такой функции может быть алгоритмически неразрешимой проблемой, т.е. не входит такая задача ни в какой класс сложности, а не только в класс P. Рассмотрим теперь предикат Af(x)=f(|x|). Для любого фиксированного n предикат равен константе. А константе сопоставляется СФЭ, сложность которой тоже равна константе. Поэтому  Af(x)  P/poly, но  его вычисление может быть алгоритмически неразрешимой проблемой.



