# ЛЗ 9 — CI/CD (GitHub Actions → Render)

Мини-приложение Flask + тесты + GitHub Actions:
- CI: pytest
- CD: Render Deploy Hook

## Как запустить локально
```bash
pip install -r requirements.txt
python app/app.py
# открой http://127.0.0.1:5000
```

## CI/CD
- При push в main Actions ставит Python 3.12, устанавливает зависимости, запускает pytest.
- Если тесты прошли — вызывается Deploy Hook Render.
- Добавь секрет `RENDER_DEPLOY_HOOK` в GitHub (URL в Render → Service → Settings → Deploy Hooks).
