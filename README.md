# av100test

## Project setup

```
yarn install
```

### Compiles and hot-reloads for development

```
yarn serve
```

### Краткое описание

```
при монтировании Settings.vue происходит захардкоженный запрос POST /login
 с моим паролем и логином для получения userId и X-User-Token. Эти данные сохраняю
  в LocalStorage для дальнейшего запроса GET /user/{userId}.
```

```
данные из GET запроса прокидываются в Account.vue для использования в placeholder inputs. чекбоксы не прокидывал,
 сложно связать значения приходящих данных и нужных чекбоксов
```
