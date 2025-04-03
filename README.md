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
```

---

## Быстрый старт

### Первая программа
```npp
fn main() {
    print("Привет, мир!")
}
```

Компиляция и запуск:
```bash
nexus build hello.nx -o hello
./hello
```

---

## Синтаксис

### Переменные
```npp
let x = 10          // Автовывод типа
let y: f64 = 3.14   // Явное указание типа
const PI = 3.1415   // Константа
```

### Функции
```npp
fn factorial(n: int) -> int {
    if n <= 1 { 1 }
    else { n * factorial(n-1) }
}
```

---

## Стандартная библиотека

### HTTP сервер
```npp
use net/http

http::Server(8080, |req| {
    if req.path == "/" {
        return Response(200, "Добро пожаловать!")
    }
}).start()
```

### Работа с JSON
```npp
use json

let data = json::parse(`{"name": "Nexus"}`)
print(data["name"])
```

---

## Компиляция

### Флаги компилятора
| Флаг | Описание |
|------|----------|
| `--opt=3` | Максимальная оптимизация |
| `--target=wasm` | Компиляция в WebAssembly |
| `--emit=asm` | Вывод ассемблерного кода |

### Профилирование
```bash
nexus build --profile app.nx
```

---

## Примеры

### Чат на WebSocket
```npp
use net/websocket

let server = WebSocketServer(8080, |client| {
    client.on_message(|msg| {
        broadcast(msg)
    })
})
```

### Умножение матриц
```npp
#[simd(avx512)]
fn matmul(a: Matrix, b: Matrix) -> Matrix {
    // Автоматическая векторизация
}
```

---

## Сообщество

- [Официальный сайт](https://nexuspp.dev)
- [GitHub](https://github.com/nexuspp)
- [Форум](https://forum.nexuspp.dev)

```bash
# Проверить версию
nexus --version
```

---

📄 **Лицензия**: Apache 2.0  
📆 **Последнее обновление**: 2023-11-15  
⚠ **Статус**: В активной разработке
```

Этот документ содержит:
1. Полное описание языка Nexus++
2. Инструкции по установке
3. Примеры кода
4. Описание стандартной библиотеки
5. Руководство по компиляции
6. Ссылки на сообщество

Файл готов к использованию на GitHub или в качестве документации для разработчиков.