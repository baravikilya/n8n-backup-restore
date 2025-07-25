# n8n Backup & Restore Workflows

Простой, но мощный набор из двух workflows для n8n, который позволяет автоматизировать процесс создания резервных копий (бэкапов) и восстановления ваших workflows и credentials. Идеально подходит для управления self-hosted n8n.


## Ключевые возможности

*   **Экспорт по требованию:** Запуск экспорта всех workflows и credentials одной кнопкой.
*   **Импорт:** Восстановление данных путем отправки файлов в чат.
*   **Простота:** Workflows используют стандартный узел `Execute Command` для выполнения нативных `n8n-cli` команд.
*   **Гибкость:** Легко адаптируется под ваши пути к файлам и нужды.


## 🚀 Установка и настройка

1.  **Клонируйте репозиторий:**
    ```bash
    git clone https://github.com/baravikilya/n8n-backup-restore.git
    ```

2.  **Импортируйте workflows:**
    *   Зайдите в ваш n8n.
    *   Нажмите `Import from File` и выберите файлы `Export_workflows_and_credentials` и `Import_workflows_and_credentials.json` из папки `workflows`.

3.  **Настройте узлы:**
    *   **Права доступа:** Убедитесь, что ваш n8n (особенно если он в Docker) имеет права на выполнение shell-команд и доступ на чтение/запись к указанным директориям.
    *   **Пути к файлам:** Убедитесь, что в узлах `Execute Command`, `Read File(s) From Disk` и `Write File to Disk` указаны реальные пути на вашем сервере.
    *   **Загрузка файлов:** Прикрепляйте файл для загрузки к сообщению чата любого содержания, предварительно соединив ноду чата с нодами загрузки credentials или workflows.