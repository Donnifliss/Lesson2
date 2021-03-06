# Разметка текста
Научимся добавлять на простейшую HTML-страницу текстовое содержание и правильно размечать его: абзацы, заголовки, подзаголовки, списки и многое другое.

Для каждого задания (далее именуется как Task*) вам потребуются input file, т.е. файлы на базе которых вы будете выполнять задание. Они названы соответственно task*.html (extension file html/css/js and etc.)

1. [Абзацы](#statement-of-work-1)
2. [Заголовки и подзаголовки](#statement-of-work-2)
3. [Неупорядоченный список](#statement-of-work-3)
4. [Упорядоченный список](#statement-of-work-4)
5. [Многоуровневый список](#statement-of-work-5)
6. [Многоуровневый список*](#statement-of-work-6)
7. [Список определений](#statement-of-work-7)
8. [Важность. Теги `<strong>` и `<b>`](#statement-of-work-8)
9. [Акцентируем внимание. Теги `<em>` и `<i>`](#statement-of-work-9)
10. [Переносы и разделители. Теги `<br>` и `<hr>`](#statement-of-work-10)
11. [Цитаты](#statement-of-work-11)
12. [Верхние и нижние индексы](#statement-of-work-12)
13. [Помечаем изменения. Теги `<del>` и `<ins>`](#statement-of-work-13)
14. [Преформатированный текст](#statement-of-work-14)
15. [Просто выделенный текст](#statement-of-work-15)
16. [Испытание: разметка статьи](#statement-of-work-16)
17. [Испытание: рецепт](#statement-of-work-17)


## Statement of work 1
### Абзацы

### Theory
На предыдущем занятии вы познакомились с тегами, необходимыми для создания простейшей HTML-страницы, и с некоторыми служебными тегами, которые не отображаются в браузере.

В этой chapter мы будем изучать теги для логической разметки текста. Использовать их можно только внутри тега `<body>`.

Начнём с простейшего тега `<p>`, с помощью которого создаются абзацы. По умолчанию абзацы начинаются с новой строки и имеют вертикальные отступы, которыми можно управлять с помощью стилей.

### Task
- Разметьте с помощью тега `<p>` ещё три предложения:
    1. «Абзац служит для ... единиц изложения.»
    2. «Выделение фразы в ... смысловой акцент.»
    3. «Для выделения абзаца ... абзацный отступ.»


## Statement of work 2
### Заголовки и подзаголовки

### Theory
Для создания структуры больших текстов обычно используются заголовки. В текстовых редакторах есть возможность выделить часть текста, найти пункт «Заголовок» нужного уровня в меню, и применить его.

В языке HTML для выделения заголовков предусмотрено целое семейство тегов: от `<h1>` до `<h6>`. Тег `<h1>` обозначает самый важный заголовок (заголовок верхнего уровня), а тег `<h6>` обозначает подзаголовок самого нижнего уровня.

На практике редко встречаются тексты, в которых встречаются подзаголовки ниже третьего уровня. Поэтому самыми часто используемыми тегами заголовков являются: `<h1>`, `<h2>` и `<h3>`.

Стоит отметить, что поисковые системы придают особое значение заголовкам, поэтому необходимо учиться правильно их использовать.

### Task
- Оберните
    1.  в тег h1 текст *«1 Заголовки»*,
    2.  в тег h2 текст *«1.1 Рекомендации по использованию»*,
    3.  в теги h3 тексты *«1.1.1 Использование H1»* и *«1.1. Использование H2-H6»*.

## Statement of work 3
### Неупорядоченный список

### Theory
Списки часто используются в различных документах. Иногда, чтобы сделать
список, пользователь просто нумерует строчки текста. Такой подход
не является хорошим, так как в документе отсутствует логическая сущность
«список».

В HTML существует семейство тегов для создания списков: неупорядоченных,
упорядоченных и списков определений. В последующих заданиях мы будем
тренироваться работать с ними.

Неупорядоченные (или маркированные) списки создаются с помощью
тега `<ul>`, который может содержать внутри себя теги `<li>`,
обозначающие «элемент списка».

### Task
- Добавьте в список изученных тегов ещё минимум три пункта.


## Statement of word 4
### Упорядоченный список

### Theory
Упорядоченный список создаётся с помощью тега `<ol>`, который может
содержать внутри себя теги `<li>`.

Если элементы неупорядоченного списка по умолчанию отмечаются маркерами,
то элементы упорядоченного списка — нумеруются.

Для упорядоченного списка можно задать атрибут start, который изменяет
начало нумерации. Например, код:

    <ol start="3">
        <li>раз</li>
        <li>два</li>
    </ol>

Приведёт к такому результату:

3.  раз
4.  два

### Task
-  Добавьте в список заголовков ещё минимум три пункта,
-  затем измените начало нумерации списка с помощью атрибута start так,
    чтобы она начиналась с числа 2 или больше.

## Statement of work 5
### Многоуровневый список

### Theory
Создать многоуровневый список весьма просто. Сначала нужно создать список первого уровня, а затем внутрь любого
элемента этого списка, между тегами `<li>` и `</li>`, добавить
список второго уровня. При этом необходимо аккуратно закрывать все теги.

Пример правильного кода:

    <ul>
        <li>1
            <ul>
                <li>1.1</li>
                <li>1.2</li>
            </ul>
        </li>
        <li>2</li>
    </ul> 

Пример кода с ошибкой:

    <ul>
        <li>1</li>
        <ul>
            <li>1.1</li>
            <li>1.2</li>
        </ul>
        <li>2</li>
    </ul>

В примере с ошибкой вложенный список вставлен не внутрь элемента списка,
а между элементами, что недопустимо.

Количество уровней в списках не ограничено. В многоуровневом списке
можно использовать как упорядоченные, так и неупорядоченные списки.

В этом задании мы потренируемся работать с многоуровневыми списками.

### Task
Создайте четырёхуровневый упорядоченный список. Достаточно, чтобы
на каждом уровне было по одному пункту.


## Statement of work 6
### Многоуровневый список*

### Theory
В этом задании вам нужно будет создать четырёхуровневый список,
наподобие этого:

1.  Разметка
    1.  Основы HTML
        1.  HTML-теги
            1.  парные
            2.  одиночные
    2.  Основы CSS
        1.  Селекторы
            1.  по типу
            2.  по классу
            3.  вложенные
    3.  Стиль кодирования
2.  Работа с фотошопом
3.  Построение сеток
4.  Декоративные элементы
5.  Введение в JavaScript
6.  Прогрессивное улучшение

### Task
Создайте четырёхуровневый упорядоченный список. Достаточно, чтобы
на каждом уровне было по одному пункту.


## Statement of work 7
### Список определений

### Theory
Список определений создаётся с помощью трёх тегов:

1.  `<dl>` обозначает сам список определений;
2.  `<dt>` обозначает термин;
3.  `<dd>` обозначает определение термина.

Теги `<dt>` и `<dd>` пишутся парами внутри `<dl>`.

Например:

    <dl>
        <dt>Термин</dt>
        <dd>Определение</dd>
        <dt>Второй термин</dt>
        <dd>И его определение</dd>
        <dt>Кошка</dt>
        <dd>Шерстяное изделие развлекательного характера</dd>
    </dl>
    
### Task
1.  Добавить четвёртый пункт с термином ul и определением Unordered
    List, неупорядоченный список.
2.  Добавить пятый пункт с термином li и определением List
    Ite[]{#anchor}m, элемент списка.


## Statement of work 8
### Важность. Теги `<strong>` и `<b>`

### Theory
Ещё раз отметим, что этот занятие посвящено **логической** разметке
текста, поэтому уделяется особое внимание смыслу элементов,
их предназначению, а не визуальному форматированию.

В предыдущих заданиях вы познакомились с элементами, которые
предназначены для разметки крупных блоков текста: заголовков, абзацев
и списков. В этом и последующих заданиях мы познакомимся с элементами,
предназначенными для разметки небольших фраз и отдельных слов.

Первые два тега предназначены, чтобы указать на важность слова или
фразы.

Тег `<strong>` определяет **важность** отмеченного текста.

Тег `<b>` предназначен для выделения текста без придания ему особой
важности.

Визуально оба тега одинаковы, они выделяют текст полужирным.

Лучше всего отличия этих тегов будут заметны людям, которые используют
специальные настройки ОС, в частности, слепым и слабовидящим. Когда они
включают функцию чтения текста, то «говорилка» будет интонацией выделять
слова с тегом `<strong>`. То же самое касается
и тегов `<em>` и `<i>`. Тег `<em>` «говорилка» будет
выделять интонацией.

Отметим, что новый смысл тегу `<b>` придали в HTML5. Раньше это был
тег, который просто делает текст полужирным. То есть он был предназначен
только для визуального форматирования.

### Task
1.  Выделите вводный абзац: заключите внутрь тега b весь текст внутри
    первого абзаца.
2.  Выделите важные детали: заключите внутрь тега strong слово
    «профессионала» во втором абзаце
3.  и фразу «настоящим ИТ-специалистом» в третьем абзаце.


## Statement of work 9
### Акцентируем внимание. Теги `<em>` и `<i>`

### Theory
Следующие два тега предназначены для акцентирования внимания на слово
или фразу.

Тег `<em>` определяет текст, на который сделан *особый акцент*,
меняющий смысл предложения.

Например, если мы хотим подчеркнуть, что Васька
не любит *питаться* укропом (он больше за тунца), а любит только *гонять
его по полу*, то разметим текст так:

Инструктор Васька любит `<em>`играть`</em>` с укропом.

Тег `<i>` обозначает текст, который отличается от окружающего
текста, но не является более важным. Обычно так
выделяют *названия*, *термины*, *иностранные слова*.

Например, если мы хотим указать, что *инспектор* — это какой-то
специальный термин, то разметим текст так:

Обычно Васька пользовался `<i>`инспектором`</i>` браузера для
поиска ошибок.

Визуально оба тега одинаковы, они выделяют текст курсивом.

Новый смысл тегу `<i>` придали в HTML5. Раньше это был просто тег
для выделения текста курсивом.

### Task
1.  Расставьте акценты: заключите внутрь тега em слово «профессию»
    в первом абзаце
2.  и слово «специалистом» в том же абзаце.
3.  Выделите с помощью тега i термин «сайте» во втором абзаце.


## Statement of work 10
### Переносы и разделители. Теги `<br>` и `<hr>`

### Theory
Иногда возникает необходимость вставить в текст перенос строки,
не создавая при этом абзац. Например, при разметке стихов или текстов
песен.

Для этого в HTML предусмотрен одиночный тег `<br>`.

Иногда этот тег используется для разбиения текста на «как бы абзацы»,
что является плохим подходом. Используйте для разметки абзацев
тег `<p>`.

Одиночный тег `<hr>` используется для того, чтобы создать
горизонтальную линию-разделитель. На внешний вид этой линии можно влиять
с помощью атрибутов, но правильней делать это с помощью CSS (это будет
изучаться на последующих занятиях).

### Task
1.  С помощью тега br добавьте восемь переносов строки в первый куплет,
2.  восемь переносов в третий.
3.  Добавьте разделители между абзацами куплетов с помощью тега hr.


## Statement of work 11
### Цитаты

### Theory
В HTML существует несколько тегов для обозначения цитат:

-   `<blockquote>` предназначен для выделения длинных цитат, которые
    могут состоять из нескольких абзацев. Тег выделяет цитату как
    отдельный блок текста с отступами.
-   `<q>` предназначен для выделения коротких цитат в предложениях.
    Текст внутри этого тега автоматически обрамляется кавычками.
-   `<cite>` используется для того, чтобы выделить источник цитаты,
    название произведения или автора цитаты.

### Task
1.  фразы *«Мастер и Маргарита»*,
2.  фразы *«Никогда ничего не просите ... Сами предложат и сами всё
    дадут!»*,
3.  и фразы *«Hasta la vista, baby»*.


## Statement of work 12
### Верхние и нижние индексы

### Theory
Следующие два тега обычно используются не для выделения слов, а для
выделения отдельных символов. Их используют для указания единиц
измерения или для написания простых формул.

Например: 20м^2^, H~2~O, X^3^+X^2^=1

Тег `<sup>` отображает текст в виде верхнего индекса.

Тег `<sub>` отображает текст в виде нижнего индекса.

Стоит отметить, что эти теги являются чисто презентационными и не имеют
собственной семантики.

Эти теги можно использовать внутри друг друга для создания более сложных
формул.

Если вам нужно вставить очень сложную формулу в HTML-документ, лучше
воспользоваться специальным языком
разметки [**MathML**](http://ru.wikipedia.org/wiki/MathML).
### Task
1.  Приведите первую формулу к виду H~2~SO~4~,
2.  вторую формулу к виду sin^2^x+cos^2^x=1.
3.  Третью формулу приведите к подходящему виду самостоятельно.


## Statement of work 13
### Помечаем изменения. Теги `<del>` и `<ins>`

### Theory
Любой документ на протяжении своей «жизни» может изменяться.
С распространением динамических веб-приложений вносить изменения
в HTML-документы стало проще простого.

Иногда возникает вопрос: а что же именно было изменено в документе, что
было добавлено, а что удалено?

Как раз для описания изменений предназначены
теги `<del>` и `<ins>`.

`<del>` выделяет текст, который был удалён в новой версии документа.

`<ins>` выделяет текст, который был добавлен в новой версии
документа.

Оба тега имеют атрибут datetime, в котором можно указать дату и время,
когда была внесена та или иная правка.

Простейшим примером применения этих тегов может служить список ошибок.
Когда ошибка исправлена, её помечают тегом `<del>`, если найдена
новая ошибка, то её добавляют в список и помечают тегом `<ins>`.

Атрибут datetime предназначен не для людей, а для компьютеров, поэтому
дату и время там пишут в стандартизованном формате. При такой разметке
программам легче разбирать документы и анализировать, когда произошли
те или иные изменения.

### Task
1.  Пометьте в списке ещё одну ошибку как исправленную с помощью del,
2.  и ещё одну как новую с помощью ins.


## Statement of work 14
### Преформатированный текст

### Theory
Наверное, вы уже заметили, как отличается отображение кода
в HTML-редакторе и в мини-браузере.

Вы можете ставить сколько угодно пробелов в HTML-коде, но браузер
отобразит их как один. Вы также можете ставить сколько угодно переносов
строки в HTML-коде, а в браузере переноса не будет, если только
не использовать специальные теги, например `<p>` или `<br>`.

Изменить это поведение браузера можно с помощью тега `<pre>`,
который обозначает «предварительно отформатированный текст». Браузер
сохраняет и отображает все пробелы и переносы, которые есть внутри
тега `<pre>`.

Наиболее часто этот тег используется при отображении примеров кода.

### Task
Заключите в тег pre весь текст внутри тега body.


## Statement of work 15
### Просто выделенный текст

### Theory
В HTML5 появился новый тег `<mark>`, который обозначает выделенный
текст.

Иногда при работе с объёмными текстами мы используем маркер, чтобы
выделять ключевые слова, идеи или что-то другое на что стоит обратить
внимание. Такое же назначение и у тега `<mark>`.

В современных браузерах текст внутри `<mark>` подсвечивается жёлтым
фоном.

### Task
Выделите три любых фрагмента скачанного текста и оформленного в виде
HTML-страницы с помощью тега mark.


## Statement of work 16
### Испытание: разметка статьи

### Theory
Чтобы пройти испытание, вам необходимо разметить текст в HTML-редакторе
точно так же, как и в образце.

При создании образца были использованы только те HTML-теги, которые
изучались в данном курсе. CSS-стили не использовались, так что изменять
код CSS-редактора нельзя.

### Task
Сделать HTML-страницу используя знания, полученные ранее. Точную копию!


## Statement of work 17
### Испытание: рецепт

### Theory
Задача аналогична предыдущей. В этом испытании использованы другие тэги
из данного занятия.

### Task
Сделать HTML-страницу используя знания, полученные ранее. Точную копию!