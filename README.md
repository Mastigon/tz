1. Опыт коммерческой разаботки на Python - 3 года. Из генераторов часто используем чанки для обработки большого кол-ва записей. __slots__, метаклассы не использовал.

2. Надо было выгрузить из БД ~1.5млн записей, обработать их и перезаписать. Первоначальный скрипт работал ~8 часов. Затем прикрутил многопроцессность - стал работать быстрее, но не достаточно. Тогда ещё прикрутил асинхронность через future pool.map_async. В конечном счёте, скрипт отрабатывал за ~20 минут.

3. За 2 года было 3 проекта на Flask. Django, FastApi не использовал.

4. Есть. Описал в ответе на 2 вопрос.

5. 2 года работал с Postgres через SqlAlchemy. Сейчас работаю на MongoDb. На текущем проекте размер БД на проде больше 100ТБ.

6. По Докеру - писал небольшие docker-файлы, создавал образ, запускал образ. Опыт на уровне разработчика, не девопса. Kubernetes - знаю, что это, но опыта нет.

7. На некоторых проектах работал с node js, но прям по минимуму. Поэтому, если только в js.

8. 
```
SELECT a.*
FROM article a
LEFT JOIN comment c ON a.id = c.article_id
WHERE c.id IS NULL;
```

```
from collections import defaultdict

worker_hours = defaultdict(list)

while True:
    try:
        line = input()
        if not line:
            break

        name, hours = line.rsplit(maxsplit=1)
        worker_hours[name].append(int(hours))
    except EOFError:
        break


for name, hours_list in worker_hours.items():
    total_hours = sum(hours_list)
    hours_str = ', '.join(map(str, hours_list))
    print(f"{name}: {hours_str}; sum: {total_hours}")
```
