# Фикс проблемы запуска Блокады через ВК\Одноклассники

Доброго времени суток, ребята

Если вы так же, как и я столкнулись с проблемой запуска игры через браузер и не имеете возможность играть через лаунчер\Steam, то вот фикс проблемы, который я сумел найти. Данный пост я разделю на две части, где в первой будет описан сам фикс, а во второй почему он работает. Очень надеюсь, что разработчики нашей игры заметят этот пост и эта информация поможет им пофиксить этот баг

## Часть 1 

Проблема этого бага в том, что при заходе в игру через браузер наблюдаем черный экран:

![Screenshot 2025-01-08 at 20 27 06](https://github.com/user-attachments/assets/53ebd5ce-82de-46d9-8ef9-453f28b90ae1)

### Решение
1. Скачайте расширение для Google Chrome под названием [fixHeader](https://chromewebstore.google.com/detail/fixheader-%E2%80%94-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B8%D1%82%D1%8C-%D0%B7%D0%B0%D0%B3%D0%BE/nmapeoicbcemgclfiacgonlpoeahacab)

![Screenshot 2025-01-08 at 20 38 38](https://github.com/user-attachments/assets/02cf0f19-247f-47f4-9f76-0acb694008fc)

4. Найдите его в расширениях Google Chrome и нажмите на него

![Screenshot 2025-01-08 at 20 30 45](https://github.com/user-attachments/assets/c6ce6271-4339-4d40-a4d1-e1d0d91a89b9)

4. Вы увидете такой интерфейс
<img width="748" alt="Screenshot 2025-01-08 at 21 03 23" src="https://github.com/user-attachments/assets/725798ef-555e-420a-aedb-8262c036e53e" />

6. Нажмите на кнопку с плюсиком Add Rule

7. Нам нужно будет добавить 6 правил. Для первого правила напишите в поля все так, как написано ниже

### ⚡⚡⚡ Внимание! Следите за тем, чтобы в полях не было лишних пробелов в начале или в конце, иначе ничего не заработает! ⚡⚡⚡

🚀 Rule name: 1

🚀 Priority: 1

🚀 Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/style.css

🚀 Вкладку Request оставьте без изменение

🚀 Во вкладке Response сделайте так, как показано на скриншоте


🚀 Key: Content-Encoding

🚀 Value: gzip

<img width="748" alt="Screenshot 2025-01-08 at 20 44 06" src="https://github.com/user-attachments/assets/b610d1ae-c717-4e85-9570-fed7af892573" />

6. Нажмите кнопку Create Rule

7. Для второго правило нужно сделать то же самое, но с небольшими изменениями. Чекайте скриншот для второго правила

Нужно заменить Rule name на 2 и заменить поле Match url patterns на https://novalinkcorp.com/webgl/Release242/WebGL.loader.js

### ⚡⚡⚡ При копировании URL-адреса следите за тем, чтобы не было пробелов перед https:// ⚡⚡⚡

<img width="639" alt="Screenshot 2025-01-08 at 20 37 09" src="https://github.com/user-attachments/assets/3516a40d-cac8-423e-8cb7-05c6cb5624e5" />

8. Для третьего правила замените Rule name, Match url patterns и обратите внимание, что поле Value во вкладке Response должно быть пустым

🚀 Rule name: 3

🚀 Match url patterns: https://novalinkcorp.com/ClassicBundles/

<img width="748" alt="Screenshot 2025-01-08 at 20 53 12" src="https://github.com/user-attachments/assets/92225d38-638f-455f-b3ef-47abeeb620d7" />

9. Четвертое:

🚀 Rule name: 4

🚀 Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/progress-bar-empty-dark.png

<img width="792" alt="Screenshot 2025-01-08 at 20 55 14" src="https://github.com/user-attachments/assets/dc11beec-3fb5-4289-9e25-91396e58140c" />

10. Пятое

🚀 Rule name: 5

🚀 Match url patterns: https://novalinkcorp.com/images/loading2017.png

<img width="748" alt="Screenshot 2025-01-08 at 20 58 08" src="https://github.com/user-attachments/assets/00e9405a-2918-4797-8153-ec0b3fb57195" />

11. И наконец шестое

🚀 Rule name: 6

🚀 Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/progress-bar-full-dark.png

<img width="792" alt="Screenshot 2025-01-08 at 20 59 01" src="https://github.com/user-attachments/assets/1f3eafd8-a01d-41bb-97af-cd868fd7500a" />







