# Фикс проблемы запуска Блокады через ВК\Одноклассники

Доброго времени суток, ребята

Если вы так же, как и я столкнулись с проблемой запуска игры через браузер и не имеете возможность играть через лаунчер\Steam, то вот фикс проблемы, который я сумел найти. Данный пост я разделю на две части, где в первой будет описан сам фикс, а во второй почему он работает. Очень надеюсь, что разработчики нашей игры заметят этот пост и эта информация поможет им пофиксить этот баг

## Часть 1 

Проблема этого бага в том, что при заходе в игру через браузер наблюдаем черный экран:

![Screenshot 2025-01-08 at 20 27 06](https://github.com/user-attachments/assets/53ebd5ce-82de-46d9-8ef9-453f28b90ae1)

### Решение
1. Скачайте расширение для Google Chrome под названием [fixHeader](https://chromewebstore.google.com/detail/fixheader-%E2%80%94-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B8%D1%82%D1%8C-%D0%B7%D0%B0%D0%B3%D0%BE/nmapeoicbcemgclfiacgonlpoeahacab)

![Screenshot 2025-01-08 at 20 38 38](https://github.com/user-attachments/assets/02cf0f19-247f-47f4-9f76-0acb694008fc)

2. Найдите его в расширениях Google Chrome и нажмите на него

![Screenshot 2025-01-08 at 20 30 45](https://github.com/user-attachments/assets/c6ce6271-4339-4d40-a4d1-e1d0d91a89b9)

3. Вы увидете такой интерфейс
<img width="748" alt="Screenshot 2025-01-08 at 21 03 23" src="https://github.com/user-attachments/assets/725798ef-555e-420a-aedb-8262c036e53e" />

4. Нажмите на кнопку с плюсиком Add Rule

5. Нам нужно будет добавить 6 правил. Для первого правила напишите в поля все так, как написано ниже

### ⚡⚡⚡ Внимание! Следите за тем, чтобы в полях не было лишних пробелов в начале или в конце, иначе ничего не заработает! ⚡⚡⚡

🚀 Rule name: 1

🚀 Priority: 1

🚀 Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/style.css

🚀 Вкладку Request оставьте без изменение

🚀 Во вкладке Response сделайте так, как показано на скриншоте


🚀 Key: Content-Encoding

🚀 Value: gzip

<img width="748" alt="Screenshot 2025-01-08 at 21 08 04" src="https://github.com/user-attachments/assets/266c6940-6fee-4c2f-a08d-d1d5068a0c44" />

6. Нажмите кнопку Create Rule

7. Для второго правило нужно сделать то же самое, но с небольшими изменениями. Чекайте скриншот для второго правила

Нужно заменить Rule name на 2 и заменить поле Match url patterns на https://novalinkcorp.com/webgl/Release242/WebGL.loader.js

### ⚡⚡⚡ При копировании URL-адреса следите за тем, чтобы не было пробелов перед https:// ⚡⚡⚡

<img width="748" alt="Screenshot 2025-01-08 at 21 09 55" src="https://github.com/user-attachments/assets/6a587c2d-1af9-462d-b2f4-236d5ae04216" />

8. Для третьего правила замените Rule name, Match url patterns и обратите внимание, что поле Value во вкладке Response должно быть пустым

🚀 Rule name: 3

🚀 Match url patterns: https://novalinkcorp.com/ClassicBundles/

<img width="748" alt="Screenshot 2025-01-08 at 20 53 12" src="https://github.com/user-attachments/assets/92225d38-638f-455f-b3ef-47abeeb620d7" />

9. Четвертое:

🚀 Rule name: 4

🚀 Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/progress-bar-empty-dark.png

<img width="748" alt="Screenshot 2025-01-08 at 21 11 16" src="https://github.com/user-attachments/assets/b4a09df8-6cfc-4cc4-8c41-dda8231b25e9" />

10. Пятое

🚀 Rule name: 5

🚀 Match url patterns: https://novalinkcorp.com/images/loading2017.png

<img width="748" alt="Screenshot 2025-01-08 at 20 58 08" src="https://github.com/user-attachments/assets/00e9405a-2918-4797-8153-ec0b3fb57195" />

11. И наконец шестое

🚀 Rule name: 6

🚀 Match url patterns: https://novalinkcorp.com/webgl/TemplateCSS/progress-bar-full-dark.png

<img width="792" alt="Screenshot 2025-01-08 at 20 59 01" src="https://github.com/user-attachments/assets/1f3eafd8-a01d-41bb-97af-cd868fd7500a" />

12. В конечно итоге получаем то, что показано на скриншоте (следите чтобы правила были включены переключателем вверху)

<img width="748" alt="Screenshot 2025-01-08 at 21 13 11" src="https://github.com/user-attachments/assets/6ab0967d-41b2-4b5e-ab9d-7e896af80bfc" />

13. По идее Блокада должна работать, но мы сталкиваемся с другой проблемой - загрузка не идет, если вы из России. Я не знаю с чем это связано и действительно ли россиянам заблокирован доступ, но эту проблему можно обойти путем включения VPN пока идет загрузка игры и выключением, когда игра загрузилась. Но так же можно попробовать очистить кэш DNS

14. Напишите в строке Google Chrome следующую строку **chrome://net-internals/#dns** и попадете на настройку кэша DNS:

![Screenshot 2025-01-08 at 21 19 02](https://github.com/user-attachments/assets/f8cfab00-ce29-41bd-9d24-53c2871db16c)

15. Нажмите кнопку Clear host cache

16. Перезапустите браузер. Проверьте, что все правила, которые мы с вами писали активны и попробуйте запустить Блокаду без VPN. Все должно работать



## Часть 2
### Почему это работает?


