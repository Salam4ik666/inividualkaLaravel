# inividualkaaravel
# Интернет-магазин молдавских hand-made изделий

## Введение
Проект представляет собой веб-приложение для продажи hand-made изделий с молдавской тематикой. Реализован с использованием фреймворка Laravel.

## Установка и запуск проекта

### Требования
- PHP >= 8.1
- Composer
- Node.js и npm
- SQLite или другая БД на выбор

### Пошаговая установка

1. Клонируйте репозиторий:
```bash
git clone https://github.com/Salam4ik666/inividualkaLaravel
cd Individual2
```
2. Установите PHP зависимости:
```bash
composer install
```
3. Установите JavaScript зависимости:
```bash
npm install
```
4. Скопируйте файл конфигурации:
```bash
cp .env.example .env
```
5. Выполните миграции и заполните базу начальными данными(если необходимо в репозитории проекта есть также SQL-команды(out.sql) для дополнительного заполнения базы данных):
```bash
php artisan migrate --seed
```

6. Запустите сборку фронтенд-ресурсов:
```bash
npm run dev
```
7. Запустите локальный сервер:
```bash
php artisan serve
```
8. Доступ к приложению
    1.  Откройте в браузере: http://localhost:8000
    2.  Введите данные для входа администратора
        -  Email: 123@mail.ru
        -  Пароль: 12345678

### Возможные проблемы


1. Если не работают стили:
```bash
npm install
npm run dev
```
2. Очистка кэша в случае проблем:
```bash
php artisan config:clear
php artisan cache:clear
php artisan view:clear
```

## Основной функционал

### 1. Главная страница
![alt text](image.png)
- Отображение категорий товаров
- Рекомендуемые продукты
- Адаптивный дизайн 
- Каталог товаров
- Авторизация
- Полезные ссылки
### 3. Карточка товара
![alt text](image-2.png)
- Детальная информация о товаре
- Цена в USD
- Возможность покупки
### 4. Личный кабинет
![alt text](image-3.png)
- Просмотр всех своих купленных подписок
- История заказов
### 4. Регистрация
![alt text](image-4.png)
### 5. Админ-панель
![alt text](image-5.png)
![alt text](image-6.png)
![alt text](image-7.png)
- Управление товарами
- Добавление товаров
- Изменение статусов заказов

## Технические особенности
1. **Аутентификация и авторизация:**
   - Регистрация пользователей
   - Разделение прав (admin/user)
   - Защита маршрутов

2. **Работа с данными:**
   - CRUD операции для товаров и категорий
   - Загрузка и хранение изображений
   - Валидация форм

3. **Интерфейс:**
   - Адаптивный дизайн
   - Интуитивно понятная навигация

### Безопасность
1. **Защита от атак:**
   - CSRF-защита для всех форм
   - XSS-защита через экранирование данных
   - SQL-инъекции предотвращаются через использование Query Builder и Eloquent
   - Валидация всех входных данных

2. **Права доступа:**
   - Middleware для проверки прав админа
   - Защита маршрутов администратора
   - Аутентификация через Laravel UI

## Использованные технологии
- Laravel (PHP)
- mySQL
- Tailwind CSS
- Blade Templates
- Laravel UI
- JavaScript

# Авторы
- Подковаль Артур
- Макаринский Андрей

## Заключение
Проект полностью реализует поставленные задачи, обеспечивая удобную платформу для продажи подписок на разные сервисы. Реализованы все необходимые функции как для покупателей, так и для администраторов магазина. Сайт создан для упращения менеджмента подписок пользователя. Он обьеденяет подписки разных сервисов в одном удобном web приложении