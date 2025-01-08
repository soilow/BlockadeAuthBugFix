# Фикс проблемы запуска Блокады через ВК\Одноклассники

Доброго времени суток, ребята

Если вы так же, как и я столкнулись с проблемой запуска игры через браузер и не имеете возможность играть через лаунчер\Steam, то вот фикс проблемы, который я сумел найти. Данный пост я разделю на две части, где в первой будет описан сам фикс, а во второй почему он работает. Очень надеюсь, что разработчики нашей игры заметят этот пост и эта информация поможет им пофиксить этот баг

## Часть 1 

Проблема этого бага в том, что при заходе в игру через браузер наблюдаем черный экран:
![Screenshot 2025-01-08 at 20 27 06](https://github.com/user-attachments/assets/53ebd5ce-82de-46d9-8ef9-453f28b90ae1)

Собственно решение:
1. Скачайте расширение для Google Chrome под названием [fixHeader](https://chromewebstore.google.com/detail/fixheader-%E2%80%94-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B8%D1%82%D1%8C-%D0%B7%D0%B0%D0%B3%D0%BE/nmapeoicbcemgclfiacgonlpoeahacab)

![Screenshot 2025-01-08 at 20 38 38](https://github.com/user-attachments/assets/02cf0f19-247f-47f4-9f76-0acb694008fc)

4. Найдите его в расширениях Google Chrome и нажмите на него

![Screenshot 2025-01-08 at 20 30 45](https://github.com/user-attachments/assets/c6ce6271-4339-4d40-a4d1-e1d0d91a89b9)

4. Вы увидете такой интерфейс (списка правил, которые представлены на скриншоте не будет - мы будем их добавлять)

<img width="792" alt="Screenshot 2025-01-08 at 20 40 58" src="https://github.com/user-attachments/assets/7cbbb3d9-757c-4624-9273-f86254851665" />

6. Нажмите на кнопку с плюсиком Add Rule

7. Нам нужно будет добавить 6 правил. Для первого правила напишите в поля все так, как написано ниже

Rule name: 1

Priority: 1

Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/style.css

Вкладку Request оставьте без изменение

Во вкладке Response сделайте так, как показано на скриншоте

<img width="748" alt="Screenshot 2025-01-08 at 20 42 32" src="https://github.com/user-attachments/assets/d23bfced-dc12-4f66-b3e3-ef61ffb2b96f" />

### Внимание! Следите за тем, чтобы в полях не было лишних пробелов в начале или в конце, иначе ничего не заработает!

6. Нажмите кнопку Create Rule

7. Для второго правило нужно сделать то же самое, но не с большими изменениями. Чекайте скриншот для второго правила
<img width="639" alt="Screenshot 2025-01-08 at 20 37 09" src="https://github.com/user-attachments/assets/3516a40d-cac8-423e-8cb7-05c6cb5624e5" />

То есть надо заменить поле Match url patterns на https://novalinkcorp.com/webgl/Release242/WebGL.loader.js


