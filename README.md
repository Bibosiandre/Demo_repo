# Demo_repo
Это репозиторий для демонстрации действующих и внедренных продуктов

This is a repository for showcasing active and deployed products.
## Face Attendance
Face Attendance — это система учёта присутствия сотрудников по IP-камерам.
Программа подключается к RTSP-потоку камеры, находит лица, распознаёт сотрудников, ведёт сессии присутствия по зонам, показывает данные на дашборде, формирует Excel-отчёты и отправляет суточные отчёты в Telegram.
<details>
  <summary><b>Основные возможности системы</b></summary>
  <ul>
    <li><b>Управление базой:</b> Добавление сотрудников и их фотографий с автоматическим созданием эмбеддингов лиц.</li>
    <li><b>Работа с видео:</b> Подключение камер по RTSP с поддержкой отдельного substream для лёгкого Live-просмотра.</li>
    <li><b>Мониторинг:</b> Live-аналитика в реальном времени с отображением рамок (bounding boxes), зон ROI и имён.</li>
    <li><b>Тайм-трекинг:</b> Автоматический учёт времени присутствия сотрудников на рабочем месте и интеллектуальное объединение коротких сессий.</li>
    <li><b>Аналитика:</b> Интерактивный дашборд с текущим присутствием сотрудников в режиме онлайн.</li>
    <li><b>Отчётность:</b> Формирование отчётов за день, неделю или кастомный период с возможностью выгрузки в Excel.</li>
    <li><b>Уведомления:</b> Telegram-бот с доступом по access-code и ежедневной автоматической отправкой отчётов в 22:00.</li>
    <li><b>Интерфейс:</b> Современный UI с полноценной поддержкой светлой и тёмной тем оформления.</li>
    <li><b>Безопасность:</b> Разграничение прав доступа с помощью ролей пользователей (admin и operator).</li>
  </ul>
</details>

<details>
  <summary>🌐 EN</summary>
  Face Attendance is an employee attendance tracking system based on IP cameras.
The software connects to the camera's RTSP stream, detects faces, recognizes employees, tracks attendance sessions by zone, displays data on a dashboard, generates Excel reports, and sends daily reports via Telegram.
  <details>
<summary><b>System Features</b></summary>
<ul>
<li><b>Database Management:</b> Add employees and their photos with automatic facial embedding generation.</li>
<li><b>Video Handling:</b> RTSP camera connectivity with support for a dedicated substream for smooth live viewing.</li>
<li><b>Monitoring:</b> Real-time live analytics displaying bounding boxes, ROI zones, and names.</li>
<li><b>Time Tracking:</b> Automatic tracking of employee workplace presence and intelligent merging of short sessions.</li>
<li><b>Analytics:</b> Interactive dashboard showing current employee presence in real time.</li>
<li><b>Reporting:</b> Report generation for daily, weekly, or custom periods with Excel export capabilities.</li>
<li><b>Notifications:</b> Telegram bot with access-code authentication and automated daily report delivery at 10:00 PM.</li>
<li><b>Interface:</b> Modern UI with full support for light and dark themes.</li>
<li><b>Security:</b> Access control based on user roles (admin and operator).</li>
</ul>
</details>
</details>

![](https://github.com/Bibosiandre/Demo_repo/blob/main/chrome_WPgiRqOg04.gif)
<h3>🛠️ Стек технологий и архитектура/Technology Stack and Architecture</h3>

<details>
  <summary>📰 <b>Веб-архитектура</b></summary>
  <ul>
    <li><b>Backend:</b> FastAPI, Uvicorn</li>
    <li><b>База данных:</b> PostgreSQL</li>
    <li><b>ORM:</b> SQLAlchemy</li>
    <li><b>Авторизация:</b> JWT (cookie), роли admin/operator</li>
  </ul>
</details>

<details>
  <summary>💻 <b>Интерфейс</b></summary>
  <ul>
    <li><b>Технологии:</b> Jinja2 templates, HTML, CSS, Vanilla JavaScript</li>
  </ul>
</details>

<details>
  <summary>👁️ <b>Компьютерное зрение и видеоаналитика</b></summary>
  <ul>
    <li><b>Базовые библиотеки:</b> PyTorch, OpenCV, NumPy</li>
    <li><b>Детекция лиц:</b> RetinaFace ResNet50</li>
    <li><b>Распознавание лиц:</b> ArcFace ResNet100 / iresnet100</li>
    <li><b>Трекинг:</b> IOU-based FaceTracker</li>
    <li><b>Видеопоток:</b> PyAV / FFmpeg (RTSP)</li>
  </ul>
</details>

<details>
  <summary>🤖 <b>Интеграция с Telegram и отчёты</b></summary>
  <ul>
    <li><b>Telegram:</b> Telegram Bot API, access-code подписка, ежедневная отправка отчётов</li>
    <li><b>Proxy для Telegram:</b> Xray-core, локальный SOCKS5 proxy</li>
    <li><b>Отчёты:</b> openpyxl, Excel</li>
  </ul>
</details>

<details>
  <summary>🖥️ <b>Окружение и аппаратные требования</b></summary>
  <ul>
    <li><b>ОС:</b> Windows</li>
    <li><b>GPU:</b> CUDA, NVIDIA RTX</li>
  </ul>
</details>

