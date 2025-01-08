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

🚀 Вкладку Request (Запрос) оставьте без изменения и переключитесь на вкладку Response (Ответ)

<img width="792" alt="Screenshot 2025-01-08 at 23 18 40" src="https://github.com/user-attachments/assets/43e95248-b420-4921-8ec3-b00488274482" />

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

![Screenshot 2025-01-08 at 21 53 02](https://github.com/user-attachments/assets/c5aaac46-6c52-40b6-a02c-7e5518580617)

Я очень надеюсь, что мой фикс кому-то поможет. Если возникли какие-то проблемы, то пишите мне в [ВК](https://vk.com/tomascan) и ищите меня в игре под ником hvost239. Удачной игры! 


## Часть 2
### Почему это работает?
Информация больше для разработчиков. Надеюсь прочитают. Я столкнулся с этим багом 4-5 дней назад после того, как очистил кэш своего браузера, но до этого все работало. Скорее всего игра подгружала кэш и ей не было дела до проблем с сервером, откуда скачивались WebGL.loader.js и компоненты игры. Вся проблема именно из-за одного сервера, а именно novalinkcorp.com. Если мы посмотрим вкладку Networks при загрузке игры, то увидим что файлы WebGL.loader.js и style.css из novalinkcorp.com загружаются и выдают статус 200, но ошибку ERR_CONTENT_DECODING_FAILED

![401263320-2fb182b1-f880-47a6-84ca-a52a92b20a07](https://github.com/user-attachments/assets/30878ed9-a942-410f-aa01-08b39cce49c6)

что как бы намекает на проблему декодирования полученных ответов от сервера. Мне стало очень интересно прогнать эти пакеты через Burp Suite, но о чудо через Burp Browser все открывалось спокойно. Спустя время я пришел к выводу, что Burp Suite каким-то образом изменяет поля ответа от сервера, потому что если убрать галочку в настройках с поля Unpack compressed responses, то наблюдаем такую же картину, как и в обычных браузерах, где Блокада не загружается

Я перепробовал разные браузеры и разные операционные системы, подменял user-agent в request, но все было тщетно. И очень интересно, что в браузере Safari не было ошибки декодирования, но появляись кракозябры, которые невозможно было декодировать

<img width="1822" alt="Screenshot 2025-01-08 at 21 34 29" src="https://github.com/user-attachments/assets/09542f51-f5a6-45e7-9eec-f64eec2a3827" />

И казалось, что решения нет, пока я не заметил в Response headers от сервера интересную картину:

![401265221-9dfc4568-59e5-4a85-b559-f311c4a1de90](https://github.com/user-attachments/assets/4baca9f6-55f4-4739-aa2e-e9ed4838bd84)

Два одинаковых поля Сontent-Encoding в одном пакете! Мне стало интересно: а что если убрать один Сontent-Encoding и оставить только один. И не прогадал. Воспользовавшись бесплатным расширением в Google Chrome Store, позволяющее заменить заголовок Responce видим, что декодирование прошло успешно для WebGL.loader.js и style.css с novalinkcorp.com

![401266223-a299c76c-9c3d-46a8-bc55-a70d4ff2a411](https://github.com/user-attachments/assets/76bc4d9c-6e76-4a31-ae22-54e6b83f421a)

Но тут возникла проблема декодирования для следующих изображений, а именно то, что у них стоит Content-Encoding gzip, но такого не должно быть, поэтому нам нужно убрать это поле из Responce Headers

![Screenshot 2025-01-08 at 21 44 04](https://github.com/user-attachments/assets/5b9f6e42-821c-4421-bbac-904fb135d430)

После того, как убрали поля Content-Encoding изображения корректно декодируются и загружаются. И на десерт: проблемы с декодированием частей игры, а именно тех, которые лежат на novalinkcorp.com/ClassicBundles

![Screenshot 2025-01-08 at 21 48 22](https://github.com/user-attachments/assets/45aa410f-c363-40e2-8820-a3a0bfce8b7e)

![Screenshot 2025-01-08 at 21 49 00](https://github.com/user-attachments/assets/4db97d2b-ece5-4d81-b433-567132f43b6a)

Здесь проблема та же: лишний Content-Encoding gzip. Удаляем его из Response Headers и все прекрасно работает за исключением того, что для входа нужно включить VPN, либо чистить кэш DNS в браузере.

Я предполагаю, что вы, разработчики, случайно настроили шифрование всех пакетов через gzip на сервере novalinkcorp.com Я не хочу утверждать, но возможно проблема в этом. Надеюсь, что эта информация поможет вам в устранении бага, если вы его фиксите :)

Спасибо, что дочитали. Удачи!







