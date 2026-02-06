# Apache Superset on Railway

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https://github.com/DavidZha1994/apache-superset-railway)

Deploy **Apache Superset 4.x** to [Railway](https://railway.app) with one click. Connect to 50+ databases with a modern analytics UI — production-ready out of the box.

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/yzha)

## Features

| Feature | Description |
|---------|-------------|
| **Superset 4.x** | Latest version with modern UI and features |
| **Database Drivers** | PostgreSQL and MySQL drivers pre-installed |
| **Auto Setup** | Admin user and database auto-configured on first boot |
| **Railway Optimized** | Production-ready with proxy fix, CSRF, and caching |
| **50+ Data Sources** | Connect any SQLAlchemy-compatible database |

## One-Click Deploy

Click the **Deploy on Railway** button above, then:

1. In your Railway project, click **+ New** → **Database** → **Add PostgreSQL**
2. Click your **Superset** service → **Variables** → add `DATABASE_URL` = `${{Postgres.DATABASE_URL}}`
3. Redeploy the service
4. Wait 2–3 minutes for initialization
5. Open your Superset service URL and login with `admin` / `admin`

> **Security**: Change the default password after first login!

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `DATABASE_URL` | Required | `${{Postgres.DATABASE_URL}}` |
| `ADMIN_USERNAME` | `admin` | Admin username |
| `ADMIN_PASSWORD` | `admin` | Admin password |
| `ADMIN_EMAIL` | `admin@superset.local` | Admin email |
| `SECRET_KEY` | Auto-generated | Flask secret key |

## Supported Databases

Connect to your data warehouses via Superset's built-in SQLAlchemy support:

PostgreSQL · MySQL · MariaDB · SQLite · ClickHouse · Trino · BigQuery · Snowflake · Redshift · and [40+ more](https://superset.apache.org/docs/configuration/databases)

## Local Development

```bash
cp .env.example .env
docker compose up -d
```

Open http://localhost:8088 and login with `admin` / `admin`.

## Resources

- [Apache Superset Documentation](https://superset.apache.org/docs/intro)
- [Railway Documentation](https://docs.railway.app/)
- [Superset Database Drivers](https://superset.apache.org/docs/configuration/databases)

## License

[Apache 2.0](LICENSE)
