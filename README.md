# Проект по дисциплине «Операционные системы»

Репозиторий содержит проект по дисциплине **«Операционные системы»** (2 курс, 3 семестр, факультет ПМ-ПУ СПбГУ).

## Описание

Демонстрационная программа на C++ с использованием WinAPI, иллюстрирующая механизмы управления потоками в ОС семейства Windows. Теоретическая основа — А. Таненбаум, Х. Бос «Операционные системы», 4-е изд.

## Демонстрируемые механизмы

- Создание и завершение потоков (`CreateThread`, `ExitThread`)
- Получение информации о потоке (`GetCurrentThreadId`, `GetCurrentProcessorNumber`)
- Ожидание завершения (`WaitForSingleObject`, `WaitForMultipleObjects`)
- Передача управления планировщику (`SwitchToThread`)
- Синхронизация через критические секции (`CRITICAL_SECTION`)
- Thread affinity (`SetThreadAffinityMask`, `SetProcessAffinityMask`)

## Сборка и запуск

```bash
# MSVC
cl /EHsc /W4 /O2 threads_demo.cpp

# MinGW
g++ -O2 threads_demo.cpp -o threads_demo.exe

# Запуск
threads_demo.exe sync    # с синхронизацией
threads_demo.exe nosync  # без синхронизации (демонстрация гонки)
