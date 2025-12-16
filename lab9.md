# Итоговый отчет

## Цель
Создание комплекса, состоящего из мобильного приложения и сайта, позволяющего легко администрировать электронные продажи книг и комфортно осуществлять покупку книг.

## Авторы проекта: **Аладко Анастасия, Будник Кирилл, Ладик Алина, Шейнин Василий.**

1. **Team Lead:** Будник Крилл.
2. **Project Manager** Ладик Алина.
3. **UX/UI-Designer** Аладко Анастасия.
4. **Mobile Developer:** Ладик Алина.
5. **Web Developer:** Аладко Анастасия.
6. **Backend Developer:** Шейнин Василий.
7. **DevOps & QA Engineer:** Шейнин Василий.
8. **Technical Writer:** Будник Кирилл.

## Стратегия дизайна

### 1. Заинтересованные стороны
- **Покупатели** (основные пользователи приложения)
- **Администраторы системы** (обработка заказов, обновление ассортимента, поддержка, управление пользователями, техническая часть)
- **Издательства и авторы** (заинтересованы в продвижении книг, новостных рассылках и предзаказах)
- **Заказчик/владелец онлайн-магазина** (бизнес-цели, прибыль)
- **Группа разработки** (ответственная за реализацию и поддержку)

### 2. Видение продукта заинтересованными лицами

#### Покупатели
- Быстрый поиск книг по автору, тематике, издательству
- Удобная покупка и оплата
- Избранное
- Подписка на новости

#### Администраторы
- Поддержка стабильности
- Контроль пользователей и базы данных

#### Издательства
- Продвижение книг через новости
- Возможность предзаказов

#### Заказчик
- Рост продаж
- Расширение клиентской базы
- Конкурентоспособность

### 3. Конфликты и противоречия
- **Ассортимент** — покупатели хотят весь спектр книг, но менеджеры вынуждены учитывать склад и бюджет
- **Удобство интерфейса vs. нагрузка на систему** — детализированный поиск и фильтры могут увеличивать нагрузку на сервер
- **Бизнес-задачи vs. пользовательский опыт** — маркетинг требует пуш-уведомлений и акций, но это может раздражать пользователей

### 4. Задачи бизнеса, маркетинга и брендинга

#### Бизнес
- Увеличить продажи
- Удерживать клиентов
- Расширить ассортимент

#### Маркетинг
- Сформировать лояльную аудиторию
- Внедрить систему персональных рекомендаций, подписки и скидки

#### Брендинг
- Создать узнаваемый и надежный онлайн-магазин
- Ассоциироваться с удобством и большим выбором

### 5. Измеримые критерии успешности
- Количество регистраций новых пользователей (ежемесячно)
- Количество совершенных заказов и предзаказов
- Доля повторных покупок (лояльность клиентов)
- Среднее время, затраченное на поиск и покупку книги
- Улучшение поиска → заказ
- Количество активных подписок на новости издательств

### 6. Технические возможности и ограничения

#### Платформа
- Веб-приложение (React, .NET, PostgreSQL/MySQL)
- Мобильное приложение (Android, Kotlin)
- Форма-фактор: десктоп и мобильная версия (адаптивный дизайн)

#### Ограничения
- Ограниченный бюджет → не сразу реализуются рекомендации на основе ML

#### Интеграции
- Платежные системы (WebPay)
- Системы доставки (Белпочта, курьерские службы)
- Email/SMS-уведомления

### 7. Представления заинтересованных лиц о пользователях

#### Основные пользователи
- Студенты и школьники (учебная литература)
- Родители (детская литература)
- Взрослые читатели (художественная литература, профессиональная литература)

#### Демография
- **Возраст**: 18–60 лет
- **Опыт**: средний уровень интернет-пользователя
- **Доступ**: мобильный и веб-доступ

### 8. Бюджет и график проекта

#### Бюджет
Ограниченный

#### Этапы реализации

| Период | Этап | Задачи |
|--------|------|--------|
| **Неделя 1–2** | Аналитика и проектирование | - Уточнение требований<br>- Финализация объектной модели, матрицы задач–ролей<br>- Проектирование интерфейсов (wireframes, прототипы) |
| **Неделя 3–4** | Архитектура и база данных | - Разработка схемы базы данных (PostgreSQL/MySQL)<br>- Настройка серверной части (.NET)<br>- Подготовка окружения для разработки |
| **Неделя 5–8** | Реализация MVP | - Каталог книг (поиск, фильтры, карточки книг)<br>- Регистрация и профиль пользователя<br>- Корзина и оформление заказа<br>- Оплата (интеграция с платёжной системой)<br>- Избранное |
| **Неделя 9–11** | Дополнительные функции | - Предзаказ книг<br>- Подписка на новости издательств<br>- Обработка заказов, добавление книг |
| **Неделя 12–13** | Тестирование и доработка | - Тестирование<br>- Исправление багов<br>- Оптимизация |
| **Неделя 14** | Подготовка к запуску | - Деплой версии<br>- Демонстрация |

**Итого**: около 4 месяцев до первого запуска

## Диаграмма бизнес процессов


## Диаграмма вариантов использования
![usecase](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/6792df8de6037109f95dfc3b903389ca987502a3/img/usecaseBookStore.svg?raw=true)

## Диаграммы деятельности

### Работа с аналитикой для админа
![admin](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/354bbe3ca42f2bbd77b0032421d1d9b6cd55d755/img/adminSeq.svg?raw=true)

### Выбор книги, используя фильтры
![filter](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/354bbe3ca42f2bbd77b0032421d1d9b6cd55d755/img/filterSeq.svg?raw=true)
![d](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/753a298cd986f1d883f99a79b29b915714e3fa98/img/Untitled%20diagram-2025-12-15-193617.svg?raw=true)
### Последовательность входа в личный кабинет
![login](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/354bbe3ca42f2bbd77b0032421d1d9b6cd55d755/img/loginSeq.svg?raw=true)

### Добавление книги в избранное с последующим уведомлением о поступлении
![stock](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/354bbe3ca42f2bbd77b0032421d1d9b6cd55d755/img/stockSeq.svg?raw=true)

### Поиск книги, оформление и оплата заказа
![payment](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/354bbe3ca42f2bbd77b0032421d1d9b6cd55d755/img/paymentSeq.svg?raw=true)


## Диаграммы классов и объектов

### Диаграмма классов, связанных с книгами
![books](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/d76238e15398a2e3e82ba6a5231e3a35d8866487/img/books.svg?raw=true)

### Диаграмма классов, связанных с выборами пользователя
![cart](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/d76238e15398a2e3e82ba6a5231e3a35d8866487/img/cart.svg?raw=true)

### Диаграмма объектов, связанных с пользователем
![object](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/d76238e15398a2e3e82ba6a5231e3a35d8866487/img/user.svg?raw=true)

### Диаграмма классов, связанных с отзывами о книге
![review](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/d76238e15398a2e3e82ba6a5231e3a35d8866487/img/review.svg?raw=true)

### Диаграмма классов для управления доступом пользователей
![user1](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/d76238e15398a2e3e82ba6a5231e3a35d8866487/img/user1.svg?raw=true)


## Диаграмма компонентов

![components](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/9afb6b5e46f7b62d2bb54059d7162923c5566bf5/img/components.svg?raw=true)


## Диаграмма развертывания
![deployment](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/75037a3ea664b4dd0bce35b461e094d31c681171/img/deployment.svg?raw=true)


## Физическая модель базы данных
![model](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/f7f30b07aed74da8908641b7314a041d7f281dcd/img/bookstore%20-%20public.png?raw=true)

## Схема базы данных
![db](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/96b837c906aab522db75a8274e7ad9547617eab6/img/erd.svg?raw=true)

## Концептуальные макеты
<img width="1286" height="1378" alt="image" src="https://github.com/user-attachments/assets/242588c4-8270-4e1c-a05e-fe0a548c8ad9" />
<img width="1859" height="906" alt="image" src="https://github.com/user-attachments/assets/84d0df24-d4da-4c27-be18-32fdc0327750" />

## Маршруты и Эндпоинты

| Сущность  | Таблица БД        | Маршрут |
|-----------|--------------------|--------|
| Auth      | Users              | POST /api/auth/sign-up |
| Auth      | Users              | POST /api/auth/sign-in |
| Auth      | Users              | POST /api/auth/sign-out |
| Auth      | Users              | POST /api/auth/refresh |
| Book      | Books              | GET /api/books/search |
| Book      | Books              | POST /api/books |
| Book      | Books              | PUT /api/books/{id} |
| Cart      | Carts, Cart_items  | GET /api/carts |
| Cart      | Carts, Cart_items  | POST /api/carts/{bookId} |
| Cart      | Carts, Cart_items  | DELETE /api/carts/{bookId} |
| Order     | Orders             | GET /api/orders |
| Order     | Orders             | POST /api/orders |
| Order     | Orders             | GET /api/orders/all |
| Order     | orders             | GET /api/orders/{orderId}/status |
| Order     | orders             | POST /api/orders/{orderId}/pay |
| Order     | orders             | PUT /api/orders/{orderId}/cancel |
| Report    | Payments    | GET /api/reports/sales |
| Review    | Reviews            | GET /api/reviews |
| Review    | Reviews            | POST /api/reviews |
| Wishlist  | Wishlists          | GET /api/wishlists |
| Wishlist  | Wishlists          | POST /api/wishlists/{bookId} |
| Wishlist  | Wishlists          | DELETE /api/wishlists/{bookId} |

| Актор        | Use Case                         | Маршрут                                 | HTTP-запрос | Аутентификация |
|--------------|----------------------------------|------------------------------------------|-------------|-----------------|
| Покупатель   | Регистрация                      | /api/auth/sign-up                        | POST        | нет             |
| Покупатель   | Вход в систему                   | /api/auth/sign-in                        | POST        | нет             |
| Покупатель   | Выход из системы                 | /api/auth/sign-out                       | POST        | да              |
| Покупатель   | Обновление токенов               | /api/auth/refresh                        | POST        | да              |
| Покупатель   | Поиск книг                       | /api/books/search                        | GET         | нет             |
| Администратор| Создать книгу                    | /api/books                               | POST        | да              |
| Администратор| Обновить книгу                   | /api/books/{id}                          | PUT         | да              |
| Покупатель   | Просмотр корзины                 | /api/carts                               | GET         | да              |
| Покупатель   | Добавить книгу в корзину         | /api/carts/{bookId}                      | POST        | да              |
| Покупатель   | Удалить книгу из корзины         | /api/carts/{bookId}                      | DELETE      | да              |
| Покупатель   | Просмотр своих заказов           | /api/orders                              | GET         | да              |
| Покупатель   | Создать заказ                    | /api/orders                              | POST        | да              |
| Администратор| Просмотр всех заказов            | /api/orders/all                          | GET         | да              |
| Покупатель   | Получить статус заказа           | /api/orders/{orderId}/status             | GET         | да              |
| Покупатель   | Оплатить заказ                   | /api/orders/{orderId}/pay                | POST        | да              |
| Покупатель   | Отменить заказ                   | /api/orders/{orderId}/cancel             | PUT         | да              |
| Администратор| Просмотр отчета по продажам      | /api/reports/sales                       | GET         | да              |
| Покупатель   | Просмотр отзывов                 | /api/reviews                             | GET         | нет             |
| Покупатель   | Создать отзыв                    | /api/reviews                             | POST        | да              |
| Покупатель   | Просмотр избранного              | /api/wishlists                           | GET         | да              |
| Покупатель   | Добавить книгу в избранное       | /api/wishlists/{bookId}                  | POST        | да              |
| Покупатель   | Удалить книгу из избранного      | /api/wishlists/{bookId}                  | DELETE      | да              |



## Реализация Веб-Сайта

| | | |
|:---:|:---:|:---:|
| ![Скриншот 1](https://github.com/user-attachments/assets/c2af3c67-6eb0-4595-843d-04b968e42f31) | ![Скриншот 2](https://github.com/user-attachments/assets/f0dac781-b1d8-499f-bc89-368340a0d8f7) | ![Скриншот 3](https://github.com/user-attachments/assets/143df3ec-8a82-4542-b551-ca9e433d7b5f) |
| ![Скриншот 4](https://github.com/user-attachments/assets/2b0338ab-da62-430a-a0a9-1b85536b4f60) | ![Скриншот 5](https://github.com/user-attachments/assets/de537e51-0dad-4ebe-8fdb-e48dd4528241) | ![Скриншот 6](https://github.com/user-attachments/assets/bce6a180-5530-43cb-a66d-f32cdb8d5bd6) |
| ![Скриншот 7](https://github.com/user-attachments/assets/3bb17ca4-b1f8-4157-a4c0-70e524bc3d8f) | ![Скриншот 8](https://github.com/user-attachments/assets/71f19763-321e-4d1f-8690-78ef92b70b70) | ![Скриншот 9](https://github.com/user-attachments/assets/b8f3fe64-6df1-405f-8926-1781e9299525) |

## Реализация Мобильного приложения
| | | |
|:---:|:---:|:---:|
| <img width="250" alt="Экран загрузки" src="https://github.com/user-attachments/assets/d582d719-3013-4a8e-a161-1121a957451e" /> | <img width="250" alt="Главный экран" src="https://github.com/user-attachments/assets/b91293a8-ab57-40f7-a4ec-8550d5cd6688" /> | <img width="250" alt="Навигация" src="https://github.com/user-attachments/assets/e3001ea8-d3db-499f-bbfe-25359b4f5009" /> |
| <img width="250" alt="Профиль" src="https://github.com/user-attachments/assets/c76e2fa7-8f37-46de-97a0-a39e0df47306" /> | <img width="250" alt="Настройки" src="https://github.com/user-attachments/assets/76c0b42a-7811-4164-8f79-3fae07026018" /> | <img width="250" alt="Уведомления" src="https://github.com/user-attachments/assets/474b7da6-f9ab-4f11-ba77-e19e430e92a9" /> |
| <img width="250" alt="Форма" src="https://github.com/user-attachments/assets/ea612e2e-9a4f-440c-a8e9-001c2d4fb8fe" /> | <img width="250" alt="Детали" src="https://github.com/user-attachments/assets/cb05dbd4-0591-4a89-901d-f73cd7171fbb" /> | |

## Тестирование

<img width="1067" height="305" alt="image" src="https://github.com/user-attachments/assets/c0be9961-51bb-43d5-90f1-426fd00ae9f8" />
<img width="1089" height="225" alt="image" src="https://github.com/user-attachments/assets/6068f3e1-8088-41cb-b57d-dfa466280f80" />

<img width="706" height="436" alt="image" src="https://github.com/user-attachments/assets/80794452-074d-48c8-bace-7f0de8f6af0e" />




















