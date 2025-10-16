План действий по созданию репозитория.
# 1. Отправить код на GitHub
git push github master

# 2. Убедиться, что репозиторий на GitHub не пуст (через браузер)

# 3. Настроить мост
git bug bridge new --name github --target github --url https://github.com/alensav/Git_Project.git --login alensav
git bug bridge auth add-token

# 4. Синхронизировать задачи
git bug bridge push github
============================================================================
============================================================================
git push github master
---------------------------------------------------------------------------
Допустим, у вас есть локальная задача:
￼
1
git bug bug new -m "Ошибка подключения" --body "ESP32 не подключается к Wi-Fi"
После:

1
git bug bridge push github
→ На GitHub в репозитории alensav/Git_Project появится Issue #1 с тем же заголовком и описанием.

Если позже вы добавите комментарий локально:
1
git bug bug comment new <ID> --body "Проверил на другой сети — работает"
и снова выполните git bug bridge push github — комментарий появится в том же Issue на GitHub.
=========================================================================
git bug bridge pull github

