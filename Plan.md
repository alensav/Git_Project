План действий по зозданию репозитория.
# 1. Отправить код на GitHub
git push github master

# 2. Убедиться, что репозиторий на GitHub не пуст (через браузер)

# 3. Настроить мост
git bug bridge new --name github --target github --url https://github.com/alensav/Git_Project.git --login alensav
git bug bridge auth add-token

# 4. Синхронизировать задачи
git bug bridge push github
