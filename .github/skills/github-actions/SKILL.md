# Навичка: github-actions

**Коли застосовувати:** Для налаштування CI (Continuous Integration) пайплайну.

**Вхідні дані:** Наявний проєкт із налаштованим CMake та тестами.

**Очікуваний результат (Виходи):**
- Створено файл `.github/workflows/ci.yml`.
- Workflow містить `matrix` для `ubuntu-latest`, `windows-latest` та `macos-latest`.
- Кроки workflow: checkout, встановлення CMake, складання проєкту (`cmake -S . -B build`, `cmake --build build`), запуск тестів (`ctest --test-dir build`).

**Як перевірити:**
Перевірити наявність файлу `.github/workflows/ci.yml` та наявність у ньому матриці з трьома ОС.

**Що робити при помилці:**
Повідомити, що CI пайплайн не згенеровано.