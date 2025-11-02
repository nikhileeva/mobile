# "Тестирование мобильных приложений".
## Проект посвящён тестированию мобильного приложения для управления задачами (Shopping List).
## В рамках работы были выполнены:
- Запуск приложения на эмуляторе Android Studio
- Тестирование по чек-листу и тест-кейсам
- Создание отчётов о дефектах в YouTrack
- Экспорт тестового прогона в формате PDF
- Экспорт отчёта по дефектам в XLSX
- Обший отчет по результатам тестирования


## Чек-лист и тест-кейсы

- [Чек-лист (Google Sheets)](https://docs.google.com/spreadsheets/d/1_h7vWK8-bZsBte3Itb75ic26aL5vvvm5D5l7bF8PMjE/edit?gid=1595243412#gid=1595243412)
- [Тест-кейсы (PDF, Qase)](https://github.com/nikhileeva/mobile/blob/main/Test%20cases.pdf)
- [Test_Run (PDF, Qase)](https://github.com/nikhileeva/mobile/blob/main/G101-Test%2Brun%2B2025_10_28%2BMobile%2BApp%2BTesting%2B(emulator)%20(1).pdf)
- [Youtrack_defects (Google Sheets)](https://docs.google.com/spreadsheets/d/10jbkudL8wP0fjygwV0h6lejhpaBOOfHs9apibKL07j0/edit?gid=1595243412#gid=1595243412)
- [General Test Report (Google Docs, PDF)](https://github.com/nikhileeva/mobile/blob/main/General%20Test%20report.pdf)

## Прокси (Charles) Safari в iOS Simulator

- **Запись трафика:** Charles + iOS Simulator (Safari)
- **Подмена удаления товара:** отправляю `DELETE /cart/{id}` → в Charles (Rewrite → Request) меняю `id` удаляемого товара на другой `id`. В итоге из корзины удаляется **другой** товар (как и требуется).
- **Показ картинки вместо контента:** через **Map Remote** перенаправляю запросы с `https://demoshopping.ru/images/*` на внешний URL изображения — в браузере отображается выбранная картинка.
- **Доказательство “мобильного” HTTPS-запроса:** во вкладке **Request → Headers** показываю строку  
  `User-Agent: Mozilla/5.0 (iPhone; CPU iPhone OS …)`; включен **Tools → No Caching…** для `demoshopping.ru`, страница обновлена.

**Видео (Google Drive):** [Simulator](https://drive.google.com/file/d/13xIcCR4g3HHW5edWDX7HaUYpX0r_89V1/view?usp=sharing)
