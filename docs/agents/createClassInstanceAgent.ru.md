# Агент создания экземпляра класса сущностей

Данный агент создает экземпляр класса сущностей.

**Класс действий:**

`action_create_class_instance`

**Параметры:**

1. `messageAddr` -- элемент класса `concept_message`.
2. `formLinkAddr` -- ссылка на информацию из всплывающего компонента.

### Пример

**Пример входной структуры:**

<img src="../images/createClassInstanceAgentInput.png"></img>

**Примеры выходной конструкции:**

Вывод об успешном создании структур.

<img src="../images/createClassInstanceAgentOutput1.png"></img>

Вывод ошибки о недопустимых или существующих параметрах.

<img src="../images/createClassInstanceAgentOutput2.png"></img>

Вывод для уведомления о завершении действия пользователем.

<img src="../images/createClassInstanceAgentOutput3.png"></img>

Результат работы агента зависит от данных, полученных от компонента. Если полученные данные верны, структуры будут созданы. В противном случае отобразится соответствующее сообщение об ошибке.

### Язык реализации агента
C++

### Результат

Возможные результаты:

* `SC_RESULT_OK` - конструкции (класс сообщения, шаблоны фраз и правило логического ответа) были успешно созданы или formLinkAddr содержит неверные данные.
* `SC_RESULT_ERROR`- внутренняя ошибка.