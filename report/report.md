# Запуск Docker контейнера

### Сборка контейнера
```bash
docker build -t glossary-fastapi .
```

### Запуск контейнера

```bash
docker run -p 8000:8000 glossary-fastapi
```

# API

1. Получение списка терминов
```
GET /terms
```
2. Получение термина по ключевому слову 
```
GET /terms/{keyword}
```

3. Добавление нового термина с описанием
```
POST /terms

body {
    keyword: string;
    title: string;
    description: string;
}
```

4. Обновление термина по ключевому слову
```
PUT /terms

body {
    keyword: string;
    title: string;
    description: string;
}
```

5. Удаление термина по ключевому слову
```
DELETE /terms
```