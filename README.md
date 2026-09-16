# AniMerge

[Русский](#русский) · [English](#english)

---

## Русский

**AniMerge** — бесплатная программа для Windows, которая собирает серии аниме с внешними озвучками, субтитрами и шрифтами в MKV. Сразу на весь сезон и без переименования файлов.

Скачанный релиз часто выглядит так: видео в корне, а озвучки и надписи лежат в подпапках с хвостами вроде `.Дубляжная`, `.RHS` или `.signs`. Батникам нужны одинаковые имена, поэтому файлы приходится переименовывать вручную. AniMerge сопоставляет их сам.

### Возможности

- **Не нужно ничего переименовывать.** Сначала программа ищет совпадение по имени видео (`Серия 07.Дубляжная.mka`), затем по номеру серии. Спорные случаи можно поправить вручную прямо в таблице.
- **Можно добавить несколько озвучек и субтитров** — каждая папка становится отдельным источником. Название, язык и флаги default/forced определяются автоматически, их можно изменить.
- **Сдвиг нумерации** — на случай, когда озвучка пронумерована 13–24, а видео 01–12.
- **Шрифты из релиза** прикрепляются к MKV, если их ещё нет среди вложений видео.
- **Все дорожки исходного видео сохраняются.** Меняются только флаги default, чтобы по умолчанию включалась выбранная озвучка. Если у этой озвучки нет файла для какой-то серии, в этой серии по умолчанию включится следующая по порядку.
- **Сборка пачкой** с прогрессом, отменой и логом mkvmerge для каждой серии. Если одна серия не собралась, остальные всё равно соберутся.
- Кириллица, скобки и длинные пути поддерживаются. Интерфейс на русском и английском.

### Установка

1. Скачайте `AniMerge-<версия>-win-x64.zip` на странице [Releases](https://github.com/ahri-X-eng/AniMerge/releases).
2. Распакуйте в любую папку и запустите `AniMerge.exe`. Установка не нужна, mkvmerge уже входит в архив.

Требования: Windows 10 или 11 (x64).

Программа не подписана цифровой подписью, поэтому при первом запуске Windows SmartScreen может показать предупреждение. Чтобы запустить программу, нажмите «Подробнее» → «Выполнить в любом случае».

### Как пользоваться

1. Перетащите папку с релизом в окно AniMerge или прямо на `AniMerge.exe`.
2. Проверьте карточки источников и таблицу сопоставления. Можно отключить лишнее, поменять язык, название, порядок дорожек или выбрать файл для отдельной серии.
3. Нажмите «Собрать». Готовые файлы появятся в папке `Completed` внутри выбранной папки.

Настройки хранятся в `%APPDATA%\AniMerge\settings.json`.

### Лицензия

AniMerge — бесплатная программа с закрытым исходным кодом, условия — в [LICENSE.txt](LICENSE.txt). Её можно использовать бесплатно, в том числе в коммерческих целях. Распространять можно только бесплатно и полным архивом без изменений.

### mkvmerge и MKVToolNix

Файлы собирает **mkvmerge** из [MKVToolNix](https://mkvtoolnix.download) (автор — Moritz Bunkus). Спасибо автору за отличный инструмент! В архив входит неизменённый `tools\mkvmerge.exe`. AniMerge запускает его как отдельную программу. mkvmerge распространяется по лицензии GNU GPL v2. Её текст и лицензии библиотек лежат в папке `licenses` архива, а исходный код соответствующей версии MKVToolNix (`mkvtoolnix-<версия>.tar.xz`) выложен в каждом релизе рядом с архивом программы. Уведомления об остальных сторонних компонентах — в `THIRD-PARTY-NOTICES.txt`.

### Связь

Telegram: [t.me/LemonYakishio](https://t.me/LemonYakishio)

---

## English

**AniMerge** is a free Windows app that merges anime episodes with external dubs, subtitles and fonts into MKV. It handles a whole season at once, with no file renaming.

A typical release has the videos in the root folder, while dubs and signs sit in subfolders with suffixes like `.Dub`, `.RHS` or `.signs`. Batch scripts need identical names, so the files have to be renamed by hand. AniMerge matches them for you.

### Features

- **No renaming.** Files are matched by video name first (`Episode 07.Dub.mka`), then by episode number. You can fix any uncertain match by hand in the table.
- **Multiple dubs and subtitle tracks** — each folder becomes its own source. Name, language and default/forced flags are detected automatically, and you can change them.
- **Episode offset** for when the dub is numbered 13–24 but the videos are 01–12.
- **Fonts from the release** are attached to the MKV unless the video already has them.
- **Every original track is kept.** Only default flags change, so your chosen dub plays by default. If that dub has no file for an episode, the next dub in order becomes the default for that episode.
- **Batch merging** with progress, cancel, and a per-episode mkvmerge log. If one episode fails, the rest still get merged.
- Cyrillic, brackets and long paths are supported. The interface is available in Russian and English.

### Installation

1. Download `AniMerge-<version>-win-x64.zip` from [Releases](https://github.com/ahri-X-eng/AniMerge/releases).
2. Extract it anywhere and run `AniMerge.exe`. No installation is needed, and mkvmerge is already included.

Requirements: Windows 10 or 11 (x64).

The app is not code-signed, so Windows SmartScreen may show a warning on first launch. To run it, click "More info" → "Run anyway".

### Usage

1. Drag the release folder onto the AniMerge window or onto `AniMerge.exe`.
2. Review the source cards and the match table. You can disable what you don't need, change the language, name or track order, or pick a file for a specific episode.
3. Click "Merge". Finished files go to the `Completed` folder inside the chosen folder.

Settings are stored in `%APPDATA%\AniMerge\settings.json`.

### License

AniMerge is closed-source freeware; see [LICENSE.txt](LICENSE.txt) for the terms. It is free to use, including for commercial purposes. You may redistribute it only free of charge, as the complete unmodified archive.

### mkvmerge and MKVToolNix

The merging is done by **mkvmerge** from [MKVToolNix](https://mkvtoolnix.download) by Moritz Bunkus — many thanks for a great tool! The archive includes an unmodified `tools\mkvmerge.exe`, which AniMerge runs as a separate program. mkvmerge is licensed under the GNU GPL v2. The license text and the licenses of its libraries are in the archive's `licenses` folder, and every release ships the matching MKVToolNix source code (`mkvtoolnix-<version>.tar.xz`) next to the app archive. Notices for the other third-party components are in `THIRD-PARTY-NOTICES.txt`.

### Contact

Telegram: [t.me/LemonYakishio](https://t.me/LemonYakishio)
