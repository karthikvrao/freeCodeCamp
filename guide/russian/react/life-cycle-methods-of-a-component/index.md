---
title: Life Cycle Methods Of A Component
localeTitle: Методы жизненного цикла компонента
---## Методы жизненного цикла компонента

Когда мы начинаем работать с компонентами, нам нужно выполнить несколько действий для обновления состояния или для выполнения некоторых действий, когда что-то изменится в этом компоненте. В этом случае методы жизненного цикла компонента пригодится! Поэтому давайте погрузиться в них в этой статье.

В широком смысле мы можем разделить методы жизненного цикла на **3** категории.

1.  монтаж
2.  обновление
3.  Размонтирование

Поскольку методы жизненного цикла являются самоочевидными, я просто упомянул имена методов. Пожалуйста, не стесняйтесь внести свой вклад в эту статью, если это необходимо.

## Монтаж:

а. `constructor()`

б. `componentWillMount()`

с. `render()`

д. `componentDidMount()`

## Обновление:

а. `componentWillRecieveProps()`

б. `shouldComponentUpdate()`

с. `componentWillUpdate()`

д. `render()`

е. `componentDidUpdate()`

## размонтирование:

а. `componentWillUnmount()`

## Некоторые интересные факты, чтобы заметить:

*   `constructor` , `componentWillMount` , `componentDidMount` и `componentWillUnmount` будут вызываться только один раз в течение жизненного цикла компонента.
*   `componentWillUpdate` и `componentDidUpdate` будет выполняться только тогда и только тогда, когда `shouldComponentUpdate` возвращает true.
*   `componentWillUnmount()` будет вызываться непосредственно перед размонтированием любого компонента и, следовательно, может использоваться для освобождения используемой памяти, закрытия любых подключений к БД и т. д.

Многие вещи можно узнать, погрузившись в кодирование. Так что заставляйте свои руки грязно кодировать.

Заметка:

> «Предупреждения об устаревании будут включены с будущим выпуском 16.x, **но устаревшие жизненные** циклы **будут продолжать работать до версии 17.** » 1
> 
> «Даже в версии 17 все равно будет возможно использовать их, но они будут сглажены префиксом« UNSAFE\_ », чтобы указать, что они могут вызвать проблемы. Мы также подготовили [автоматический сценарий, чтобы переименовать их](https://github.com/reactjs/react-codemod#rename-unsafe-lifecycles) в существующий код». 1

Другими словами, эти методы жизненного цикла previouse будут по-прежнему доступны как:

*   `UNSAFE_componentWillMount`
*   `UNSAFE_componentWillReceiveProps`
*   `UNSAFE_componentWillUpdate`

## Новые методы жизненного цикла

Новые методы жизненного цикла будут введены в Реакт 17

*   `getDerivedStateFromProps` будет более безопасной альтернативой `componentWillReceiveProps` .
*   `getSnapshotBeforeUpdate` будет добавлен для поддержки безопасного чтения свойств из обновлений DOM.

Многие вещи можно узнать, погрузившись в кодирование. Так что заставляйте свои руки грязно кодировать.

### источники

1.  [Вон, Брайан. «React v16.3.0: новый жизненный цикл и контекстный API». 29 марта 2018 года. Доступ: 22 мая 2018 года.](https://reactjs.org/blog/2018/03/29/react-v-16-3.html)

### Ресурсы

[Обновление асинхронного рендеринга](https://reactjs.org/blog/2018/03/27/update-on-async-rendering.html)