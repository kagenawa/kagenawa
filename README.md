### Гасилин Дмитрий — инженер по безопасности AI/LLM-продуктов

Основатель Disform — первого в РФ агентства аудита безопасности
LLM-продуктов. Резидент акселератора Радар. Регистрирую собственный фреймворк
**Spider** в Роспатенте как программу для ЭВМ.

#### Что делаю

- Полный цикл аудитов AI-продуктов: брифинг → договор → прогон → разбор отчёта → фиксы
- Собственный движок Spider на Python: 8 модулей веб-проверок, 24+ векторов атак
  на LLM, multi-turn chains, indirect injection через подменные документы,
  anti-hallucination фильтр с fact-check CVE по NVD
- 152-ФЗ pre-check модуль (6 детекторов)
- Continuous monitoring с алертами в Telegram/SMTP
- 631 pytest-кейс, precision 1.0 / recall 1.0 на размеченном корпусе

#### Опыт

- **Disform** (декабрь 2025 — сейчас) — основатель, инженер по безопасности AI-продуктов
- **Эддреа** (5 мес) — инженер L3 сетевой диагностики, обучил локальную LLM на MD-базе знаний с RAG
- **Код безопасности** (7 мес, стажировка) — диагностика VPN на ViPNet, PKI, X.509, Wireshark

#### Стек

`Python` `asyncio` `Playwright` `pytest` `Anthropic API` `Postgres` `SQLite`
`Docker` `Linux` `Wireshark` `REST` `GraphQL` `OWASP LLM Top 10` `CVSS 3.1` `NVD`

`TCP/IP` `BGP` `VLAN` `Cisco` `MikroTik` `Zabbix` `ViPNet` `PKI`

#### Реальные кейсы

- bnlab.tech — полный аудит LLM-продукта
- easyplaner.ru — web + 152-ФЗ pre-check
- reels-boss.io — IDOR в админ-панелях, обход RLS в Supabase, утечки БД

Поиск админок и критов в стандартном стеке ЦА (Supabase/Next.js): ~10 минут.
Эксплуатация утечек БД (клиенты/платежи): до 30 минут на стандартном стеке.

#### Контакты

- Telegram: [@guttergeishablues](https://t.me/guttergeishablues)
- Email: gasilin-88@mail.ru
- Сайт: [disform.ru](https://disform.ru)

---

> Открыт к позициям junior/middle в ИБ: AppSec, SOC L1, Network Security, СКЗИ.
> Готов закрывать сложные кейсы автономно, есть привычка к методической работе и аудит-трейлу.
