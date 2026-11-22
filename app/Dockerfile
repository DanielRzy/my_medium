FROM python:3.11-slim

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /app

COPY . .

RUN uv sync --frozen --no-dev

CMD ["uv", "run", "python", "my_medium/manage.py", "runserver", "0.0.0.0:8000"]

