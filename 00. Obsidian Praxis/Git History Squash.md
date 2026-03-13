
```shell
# 1. Удаление текущего локального репозитория
rm -rf .git

# 2. Новая инициализация
git init
git add .
git commit -m "Initial Obsidian vault backup"

# 3. Подключите удаленный репозиторий
git remote add origin https://github.com/yourusername/your-obsidian-repo.git
git branch -M main

# 4. Force push (перезапишет историю)
git push -f origin main
```