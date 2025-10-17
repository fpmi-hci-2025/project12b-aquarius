# Логическая модель базы данных
## Authors

| Поле       | Смысл поля         | Тип данных                     |
|------------|------------------|--------------------------------|
| Id         | Уникальный идентификатор автора | uuid NOT NULL                  |
| FirstName  | Имя автора        | text NOT NULL                  |
| LastName   | Фамилия автора    | text NOT NULL                  |
| CreatedAt  | Дата создания записи | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи | timestamp with time zone NOT NULL |

## Book-Author

| Поле     | Смысл поля           | Тип данных        |
|----------|--------------------|-----------------|
| BookId   | Идентификатор книги | uuid NOT NULL   |
| AuthorId | Идентификатор автора | uuid NOT NULL  |

## Book-Genre

| Поле     | Смысл поля           | Тип данных        |
|----------|--------------------|-----------------|
| BookId   | Идентификатор книги | uuid NOT NULL   |
| GenreId  | Идентификатор жанра | uuid NOT NULL  |

## Books

| Поле            | Смысл поля                    | Тип данных                     |
|-----------------|-------------------------------|--------------------------------|
| Id              | Уникальный идентификатор книги | uuid NOT NULL                  |
| ISBN            | Международный стандартный номер книги | character varying(20) NOT NULL |
| Title           | Название книги               | character varying(500) NOT NULL |
| Description     | Описание книги               | text                           |
| PublicationYear | Год публикации               | integer                        |
| PageCount       | Количество страниц           | integer                        |
| Weight          | Вес книги                     | integer                        |
| Price           | Цена книги                     | numeric(18,2) NOT NULL         |
| CoverImageUrl   | Изображение обложки (в байтах)| bytea                          |
| PublisherId     | Идентификатор издателя       | uuid NOT NULL                  |
| CreatedAt       | Дата создания записи          | timestamp with time zone NOT NULL |
| UpdatedAt       | Дата обновления записи        | timestamp with time zone NOT NULL |
| CartItemId      | Идентификатор элемента корзины | uuid                           |
| Quantity        | Количество экземпляров       | integer DEFAULT 0 NOT NULL    |

## CartItems

| Поле       | Смысл поля             | Тип данных                     |
|------------|----------------------|--------------------------------|
| Id         | Уникальный идентификатор | uuid NOT NULL                  |
| CartId     | Идентификатор корзины | uuid NOT NULL                  |
| CreatedAt  | Дата создания записи  | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи| timestamp with time zone NOT NULL |

## Carts

| Поле       | Смысл поля             | Тип данных                     |
|------------|----------------------|--------------------------------|
| Id         | Уникальный идентификатор корзины | uuid NOT NULL                  |
| UserId     | Идентификатор пользователя      | uuid NOT NULL                  |
| CreatedAt  | Дата создания записи  | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи| timestamp with time zone NOT NULL |

## Genres

| Поле       | Смысл поля       | Тип данных                     |
|------------|----------------|--------------------------------|
| Id         | Уникальный идентификатор жанра | uuid NOT NULL                  |
| Name       | Название жанра  | text NOT NULL                  |
| CreatedAt  | Дата создания записи | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи | timestamp with time zone NOT NULL |



## OrderItems

| Поле       | Смысл поля                  | Тип данных                     |
|------------|----------------------------|--------------------------------|
| Id         | Уникальный идентификатор   | uuid NOT NULL                  |
| Quantity   | Количество книг в заказе    | integer NOT NULL               |
| OrderId    | Идентификатор заказа        | uuid NOT NULL                  |
| BookId     | Идентификатор книги         | uuid NOT NULL                  |
| CreatedAt  | Дата создания записи        | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи      | timestamp with time zone NOT NULL |

## Orders

| Поле             | Смысл поля                     | Тип данных                     |
|------------------|--------------------------------|--------------------------------|
| Id               | Уникальный идентификатор заказа | uuid NOT NULL                  |
| CustomerNotes    | Заметки клиента               | text                           |
| UserId           | Идентификатор пользователя     | uuid NOT NULL                  |
| Status           | Статус заказа                  | text NOT NULL                  |
| PaymentId        | Идентификатор платежа          | uuid                           |
| ShippingAddressId| Идентификатор адреса доставки  | uuid NOT NULL                  |
| CreatedAt        | Дата создания записи           | timestamp with time zone NOT NULL |
| UpdatedAt        | Дата обновления записи         | timestamp with time zone NOT NULL |

## Payments

| Поле            | Смысл поля                   | Тип данных                     |
|-----------------|-----------------------------|--------------------------------|
| Id              | Уникальный идентификатор     | uuid NOT NULL                  |
| TransactionNumber| Номер транзакции            | character varying(100) NOT NULL |
| PaymentMethod   | Метод оплаты                | character varying(50) NOT NULL |
| Amount          | Сумма платежа               | numeric(18,2) NOT NULL         |
| OrderId         | Идентификатор заказа         | uuid NOT NULL                  |
| CreatedAt       | Дата создания записи        | timestamp with time zone NOT NULL |
| UpdatedAt       | Дата обновления записи      | timestamp with time zone NOT NULL |

## PickupAddresses

| Поле        | Смысл поля              | Тип данных                     |
|------------|-----------------------|--------------------------------|
| Id         | Уникальный идентификатор | uuid NOT NULL                  |
| AddressLine1| Адрес (строка)         | character varying(255) NOT NULL|
| City       | Город                   | character varying(100) NOT NULL|
| Country    | Страна                  | character varying(100) NOT NULL|
| CreatedAt  | Дата создания записи     | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи   | timestamp with time zone NOT NULL |

## Publishers

| Поле         | Смысл поля                  | Тип данных                     |
|--------------|----------------------------|--------------------------------|
| Id           | Уникальный идентификатор    | uuid NOT NULL                  |
| Name         | Название издателя          | character varying(255) NOT NULL|
| Description  | Описание издателя          | text                           |
| ContactEmail | Email издателя             | character varying(255)         |
| CreatedAt    | Дата создания записи        | timestamp with time zone NOT NULL |
| UpdatedAt    | Дата обновления записи      | timestamp with time zone NOT NULL |



## Reviews

| Поле       | Смысл поля              | Тип данных                     |
|------------|-----------------------|--------------------------------|
| Id         | Уникальный идентификатор | uuid NOT NULL                  |
| Rating     | Рейтинг книги           | integer NOT NULL               |
| Comment    | Комментарий             | text                           |
| BookId     | Идентификатор книги     | uuid NOT NULL                  |
| UserId     | Идентификатор пользователя | uuid NOT NULL               |
| CreatedAt  | Дата создания записи    | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи  | timestamp with time zone NOT NULL |

## Roles

| Поле       | Смысл поля             | Тип данных                     |
|------------|----------------------|--------------------------------|
| Id         | Уникальный идентификатор роли | uuid NOT NULL                  |
| Name       | Название роли          | character varying(50) NOT NULL|
| CreatedAt  | Дата создания записи   | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи | timestamp with time zone NOT NULL |

## User-Role

| Поле     | Смысл поля               | Тип данных        |
|----------|------------------------|-----------------|
| UserId   | Идентификатор пользователя | uuid NOT NULL  |
| RoleId   | Идентификатор роли       | uuid NOT NULL  |

## UserTokens

| Поле                     | Смысл поля                     | Тип данных                     |
|---------------------------|--------------------------------|--------------------------------|
| Id                        | Уникальный идентификатор токена | uuid NOT NULL                  |
| RefreshToken              | Токен обновления                | character varying(500)         |
| RefreshTokenExpirationDate| Дата истечения токена           | timestamp with time zone       |
| CreatedAt                 | Дата создания записи            | timestamp with time zone NOT NULL |
| UpdatedAt                 | Дата обновления записи          | timestamp with time zone NOT NULL |

## Users

| Поле        | Смысл поля                   | Тип данных                     |
|------------|------------------------------|--------------------------------|
| Id         | Уникальный идентификатор      | uuid NOT NULL                  |
| Email      | Email пользователя            | character varying(255) NOT NULL|
| PasswordHash| Хэш пароля                   | character varying(500) NOT NULL|
| FirstName  | Имя пользователя             | text                           |
| LastName   | Фамилия пользователя         | text                           |
| Phone      | Телефон                       | text                           |
| DateOfBirth| Дата рождения                | date                           |
| WishlistId | Идентификатор списка желаний | uuid                           |
| TokensId   | Идентификатор токена         | uuid NOT NULL                  |
| CreatedAt  | Дата создания записи          | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи        | timestamp with time zone NOT NULL |
| CartId     | Идентификатор корзины         | uuid DEFAULT '00000000-0000-0000-0000-000000000000' NOT NULL |

## Wishlist-Book

| Поле       | Смысл поля               | Тип данных        |
|------------|------------------------|-----------------|
| WishlistId | Идентификатор списка желаний | uuid NOT NULL |
| BookId     | Идентификатор книги       | uuid NOT NULL  |

## Wishlists

| Поле       | Смысл поля                | Тип данных                     |
|------------|-------------------------|--------------------------------|
| Id         | Уникальный идентификатор  | uuid NOT NULL                  |
| UserId     | Идентификатор пользователя | uuid NOT NULL                  |
| CreatedAt  | Дата создания записи       | timestamp with time zone NOT NULL |
| UpdatedAt  | Дата обновления записи     | timestamp with time zone NOT NULL |
# Физическая модель базы данных
![model](https://github.com/fpmi-hci-2025/project12b-aquarius/blob/f7f30b07aed74da8908641b7314a041d7f281dcd/img/bookstore%20-%20public.png?raw=true)
