---
lang: ru
layout: home
lang-ref: index
---

# Разработка ОТРС

## Установка расширения (.opm)

1. После установки проверь что настройки из `Kernel/Config/Files/XML/` были
   применены.

## Настройка полей по которым будет искать пользователей CustomerSearch()

В `Kernel/Config/Defaults.pm` или `Kernel/Config.pm` в поле
`CustomerUserSearchFields` прописать список полей для поиска пользователей:

```
CustomerUserSearchFields => [ 'login', 'first_name', 'last_name', 'customer_id' ],
```

Поля, они же столбцы описи `customer_user`, указываем как есть с маленькой буквы, а изменяемые
поля уже по их имени с учётом написания букв.

Если указать неправильно хотя бы одно значение, то весь поиск не будет работать.
