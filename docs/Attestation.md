## Урок 0. Общие вопросы

### Архитектура web приложений

**Что такое трёхуровневая архитектура web приложений? Какие компоненты в ней есть? Для чего нужны эти компоненты?**

Трёхуровневая архитектура веб-приложений — это модель, в которой пользовательский интерфейс, функциональная логика процесса, хранение компьютерных данных и доступ к ним разрабатываются и поддерживаются как независимые модули.

Клиент — это компонент комплекса, предоставляемый конечному пользователю. На этот уровень обычно выносится только простейшая бизнес-логика: интерфейс авторизации, алгоритмы шифрования, проверка вводимых значений на допустимость и соответствие формату, несложные операции с данными.
Сервер приложений располагается на втором уровне, на нём сосредоточена большая часть бизнес-логики.
Сервер баз данных обеспечивает хранение данных и выносится на отдельный уровень, реализуется, как правило, средствами систем управления базами данных, подключение к этому компоненту обеспечивается только с уровня сервера приложений.

Клиент позволяет пользователям взаимодействовать с сервером и внутренней службой через браузер. Код находится в браузере, получает запросы и предоставляет пользователю необходимую информацию.
Веб-сервер обрабатывает бизнес-логику и запросы пользователей, направляя запросы к нужному компоненту и управляя всеми операциями приложения.
Сервер баз данных предоставляет необходимые данные для приложения и решает задачи, связанные с данными.

**Какую роль выполняет пользовательский интерфейс в веб-приложении?**

Пользовательский интерфейс (UI) - это система взаимодействия между пользователем и программным обеспечением или веб-сайтом. UI включает в себя все элементы, которые позволяют пользователю управлять и взаимодействовать с продуктом или услугой, такие как кнопки, меню, формы и т. д.



### GitLab + Git

**Какими способами можно создать локальный репозиторий?**

В существующем каталоге. Для этого нужно перейти в каталог, который не находится под версионным контролем Git, и выполнить команду git init. Эта команда создаст в текущем каталоге новый подкаталог с именем .git, содержащий все необходимые файлы репозитория.
Клонирование существующего репозитория. Для этого используется команда git clone. Она позволяет получить копию существующего Git-репозитория.

**Как исключить из истории Git определенные файлы, которые не должны попасть в репозиторий?**

Чтобы исключить из истории Git определённые файлы, которые не должны попасть в репозиторий, можно использовать файл .gitignore. Его нужно создать в корне проекта и добавить в репозиторий. В этот файл с помощью текстового редактора добавляются имена файлов и директорий, которые надо игнорировать.

Ещё один способ — отредактировать файл .git/info/exclude. В нём можно определить персональные шаблоны игнорирования для конкретного репозитория. Например, если есть пользовательские настройки для ведения журналов или специальные инструменты разработки, которые создают файлы в рабочем каталоге репозитория, их можно добавить в .git/info/exclude, чтобы они случайно не попали в коммит.

Если файл уже добавлен в репозиторий Git и нужно прекратить его отслеживать, можно удалить его из индекса с помощью команды git rm с параметром --cached. Это приведёт к удалению файла из репозитория и предотвращению отслеживания дальнейших изменений Git.