Задание 1
Для сохранения уроков и курсов реализуйте дополнительную проверку на отсутствие в материалах ссылок на сторонние ресурсы, кроме youtube.com.
То есть ссылки на видео можно прикреплять в материалы, а ссылки на сторонние образовательные платформы или личные сайты — нельзя.
Создайте отдельный файл validators.py, реализуйте валидатор, проверяющий ссылку, которую пользователь хочет записать в поле урока с помощью класса или функции.
Интегрируйте валидатор в сериализатор.
Если вы используете функцию-валидатор — указанием валидаторов для поля сериализатора validators=[ваш_валидатор].
Если вы используете класс-валидатор — указанием валидаторов в class Meta:
validators = [ваш_валидатор(field='поле_которое_валидируем')].

Задание 2
Добавьте модель подписки на обновления курса для пользователя.
Модель подписки должна содержать следующие поля: «пользователь» (FK на модель пользователя), «курс» (FK на модель курса). Можете дополнительно расширить модель при необходимости.
Вам необходимо реализовать эндпоинт для установки подписки пользователя и на удаление подписки у пользователя.

Задание 3
Реализуйте пагинацию для вывода всех уроков и курсов.
Пагинацию реализуйте в отдельном файле paginators.py. Можно реализовать один или несколько классов пагинатора. Укажите параметры 
page_size, page_size_query_param, max_page_size для класса PageNumberPagination. Количество элементов на странице выберите самостоятельно. Интегрируйте пагинатор в контроллеры, используя параметр pagination_class.

Задание 4
Напишите тесты, которые будут проверять корректность работы CRUD уроков и функционал работы подписки на обновления курса.
В тестах используйте метод setUp для заполнения базы данных тестовыми данными. Обработайте возможные варианты взаимодействия с контроллерами пользователей с разными правами доступа. Для аутентификации пользователей используйте self.client.force_authenticate(). 

Сохраните результат проверки покрытия тестами.

Дополнительное задание
Напишите тесты на все имеющиеся эндпоинты в проекте.
