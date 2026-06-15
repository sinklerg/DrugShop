# RefactorumDrug

Плагин для Paper/Purpur 1.20.4 и Java 17.

## Быстрый запуск

Готовый jar уже лежит здесь:

```text
build/libs/RefactorumDrug-1.3.0.jar
```

Его можно сразу положить в папку `plugins` на сервере.

## Сборка на Windows

Откройте PowerShell или CMD именно в этой папке проекта и выполни:

```powershell
.\gradlew.bat clean build
```

Или просто запустите файл:

```text
build.bat
```

После сборки готовый jar будет здесь:

```text
build/libs/RefactorumDrug-1.3.0.jar
```

## Важно

Не запускайте `gradle clean build` из папки `Desktop`. Команду нужно выполнять из папки, где лежат файлы:

```text
build.gradle.kts
settings.gradle.kts
gradlew.bat
src
```

## Команды

`/drugshop` - открыть магазин.

`/drugshop <страница или id>` - открыть нужную страницу магазина.

`/drugshop addiction` - показать личный уровень зависимости.

`/drugshop addiction <ник>` - показать зависимость другого онлайн игрока. Нужно право `drugshop.admin`.

`/drugshop addiction reset <ник>` - сбросить зависимость онлайн игрока. Нужно право `drugshop.admin`.

`/drugshop addiction set <ник> <уровень>` - выставить степень зависимости онлайн игроку. Нужно право `drugshop.admin`.

`/drugshop reload` - перезагрузить `config.yml` и `messages.yml`. Нужно право `drugshop.admin`.

## Права

`drugshop.use` - доступ к магазину и просмотру своей зависимости.

`drugshop.admin` - перезагрузка конфига, просмотр, сброс и выставление зависимости игроков.

## Валюта

В `config.yml` есть раздел `currency`.

`mode: VAULT` - покупка идет через экономику сервера. Нужны Vault и любой экономический плагин.

`mode: ITEM` - покупка идет за предметы из раздела `currency.item`.
