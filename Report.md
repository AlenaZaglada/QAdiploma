# Отчет о проведенном тестировании

Проведено автоматическое тестирование комплексного сервиса покупки тура, взаимодействующего с СУБД и API Банка.

Общее количество тест кейсов: 54.

Позитивных тестов 20, негативных 34.

![image](https://github.com/AlenaZaglada/QAdiploma/assets/121796172/09f624a1-2743-4245-86c0-1e2231a05319)


# Общие рекомендации

1. Исправить визуальные и орфографические ошибки [ошибка в слове Марракеш](https://github.com/AlenaZaglada/QAdiploma/assets/121796172/f74fa991-e4e6-4e35-a49b-68dd62ecdf99)
2. Очень много дефектов связано с неверными сообщениями об ошибках, это необходимо скорректировать.
3. Для поля "Владелец" ввести ограничение на вводимые символы - только английские буквы, нечувствительные к регистру.
4. Сделать кнопку "Продолжить" неактивной, если есть пустые и/или неправильно заполненные поля.

Полный список найденных дефектов находится в  ссылка [Issues](https://github.com/AlenaZaglada/QAdiploma/issues)