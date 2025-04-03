# Nexus++ - Документация

![Лого Nexus++](https://nexuspp.dev/logo.png)

## Оглавление
1. [Установка](#установка)
2. [Быстрый старт](#быстрый-старт)
3. [Синтаксис](#синтаксис)
4. [Стандартная библиотека](#стандартная-библиотека)
5. [Компиляция](#компиляция)
6. [Примеры](#примеры)
7. [Сообщество](#сообщество)

---

## Установка

### Системные требования
- Процессор x86_64 или ARM64
- 4 ГБ ОЗУ
- 2 ГБ свободного места

### Скачать
| Платформа | Установщик | Контрольная сумма |
|-----------|------------|-------------------|
| Windows | [nexuspp-1.0-x64.exe](https://dl.nexuspp.dev/win) | `sha256: a1b2...` |
| macOS | [nexuspp-1.0.dmg](https://dl.nexuspp.dev/mac) | `sha256: c3d4...` |
| Linux | [nexuspp_1.0_amd64.deb](https://dl.nexuspp.dev/linux) | `sha256: e5f6...` |

### Сборка из исходников
```bash
git clone https://github.com/nexuspp/compiler
cd compiler
./configure --optimize=native
make -j8
sudo make install