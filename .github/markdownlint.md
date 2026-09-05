# markdownlint

Проверка Markdown-файлов домашних заданий через [markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2).

Линтер смотрит только файлы, имя которых начинается с `HW` (без учёта регистра): `HW01.md`, `hw02.md`, `Hw10.MD`. README и этот файл не проверяются. Набор файлов задаётся в [`.markdownlint-cli2.jsonc`](../.markdownlint-cli2.jsonc).


## PowerShell

```powershell
docker run --rm -v "${PWD}:/workdir" davidanson/markdownlint-cli2:v0.23.2
```

Автоисправление правил:

```powershell
docker run --rm -v "${PWD}:/workdir" davidanson/markdownlint-cli2:v0.23.2 --fix
```

Если `--fix` завершится с ошибкой доступа к файлам, добавьте `-u root` после `docker run`.

## Linux (bash / zsh)

```bash
docker run --rm -v "$PWD:/workdir" davidanson/markdownlint-cli2:v0.23.2
```

```bash
docker run --rm -v "$PWD:/workdir" davidanson/markdownlint-cli2:v0.23.2 --fix
```
