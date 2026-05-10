# Дмитрий Гасилин

**Founder of [disform.ru](https://disform.ru) — first AI/LLM security audit agency in Russia.**
Building Spider — proprietary audit engine for AI products. Resident of Radar accelerator.
Spider registered in Rospatent as a software product.

[![Telegram](https://img.shields.io/badge/Telegram-@guttergeishablues-26A5E4?style=flat&logo=telegram&logoColor=white)](https://t.me/guttergeishablues)
[![Email](https://img.shields.io/badge/Email-gasilin--88@mail.ru-D44638?style=flat&logo=maildotru&logoColor=white)](mailto:gasilin-88@mail.ru)
[![Website](https://img.shields.io/badge/disform.ru-Visit-0030FF?style=flat&logo=safari&logoColor=white)](https://disform.ru)

---

## Чем занимаюсь

Веду полный цикл аудитов безопасности AI-продуктов: от первого письма клиенту
до закрытых фиксов. Сам пишу движок, сам общаюсь с заказчиком, сам разбираю
отчёт, сам помогаю с фиксами. Контракты, NDA, письменные согласия, аудит-трейлы.
Юридическая чистота — обязательная часть работы (272 УК).

Параллельно — расширенный поиск веб-уязвимостей: IDOR в админ-панелях,
обход RLS в Supabase, утечки баз данных, незащищённые RPC, утечки ключей
в JS-бандлах. Стандартная воронка: 10 минут на админку, 30 минут на эксплуатацию
утечки БД на типовом стеке клиента.

## Spider — собственный фреймворк аудита

Python, ~30k LOC, 631 pytest-кейс на CI. Регистрирую в Роспатенте.

**LLM-уровень**
- 24+ векторов атак: prompt-leak, jailbreak, indirect injection через подменные документы, RAG poisoning, output manipulation, tool exploitation
- Multi-turn chains
- Adapters: REST (httpx), headless (Playwright), Telegram (Telethon), GraphQL с детектором auth-bypass
- Кастомные адаптеры под n8n, Dify, Flowise, GigaChat, YandexGPT
- Continuous monitoring с алертами в Telegram/SMTP, SQLite per client

**Web-уровень (8 модулей)**
- TLS/SSL audit, утекшие секреты в JS-бандлах, маппинг REST/GraphQL эндпоинтов,
  fingerprinting фреймворков с fact-check по NVD, rate-limit + token-exhaustion,
  email header injection, опционально nuclei
- Pre-flight calibration: детект CAPTCHA/WAF/rate-limit ДО запуска атак

**Защита от false-positive**
- Verification critical findings: consensus voting 2-of-2
- Baseline-сравнение: понижение confirmed → potential при совпадении с нейтральными ответами
- Snapshot before/after: meta-Finding если target изменил состояние во время атак
- Anti-hallucination: whitelist 8 фреймворков + fact-check CVE по локальному NVD-кешу
- На размеченном корпусе из 54 кейсов: precision 1.0 / recall 1.0

**152-ФЗ pre-check** — отдельный модуль с 6 детекторами: политика, право на удаление,
data residency, аудит-логи, утечки ПДн через ответы LLM, передача за рубеж.

## Реальные кейсы

| Клиент | Стек | Что нашёл |
|---|---|---|
| bnlab.tech | LLM-чат-бот | prompt-leak, indirect injection, утечки методологии |
| easyplaner.ru | Next.js + Supabase | веб-уязвимости + 152-ФЗ нарушения |
| reels-boss.io | Next.js + Supabase + AI | IDOR в админке, обход RLS, эксплуатация утечки БД (клиенты + платежи) |

Сократил время одного аудита с 5 дней ручной работы до 1 дня через автоматизацию.

## Чем подкреплено

- Резидент акселератора **Радар**
- Регистрация Spider в **Роспатенте** как программа для ЭВМ
- Заявка на товарный знак **disform**
- Партнёрства с двумя студиями разработки и юрбюро по 152-ФЗ
- Один из клиентов — резидент **МГУ**

## Опыт до Disform

**Эддреа** — инженер L3 сетевой диагностики (5 мес). TCP/IP, BGP, VLAN, MikroTik, Cisco, Zabbix. Закрыл собственный AI-ассистент: собрал базу знаний в векторную БД, поднял локальную LLM с RAG поверх. Ассистент отвечал по MD-докам только со ссылкой на источник. Снял типовые вопросы с сеньоров на период адаптации. Среднее время решения по своей зоне сократил на треть.

**Код безопасности** — стажировка в крупном вендоре СКЗИ (7 мес). Диагностика VPN-каналов на ViPNet, разбор сбоев аутентификации и шифрования, работа с PKI, X.509, токенами. Wireshark постоянно — без пакетного анализа правду не достанешь. Написал скрипт автосбора диагностики, первичный разбор инцидента ускорился раза в три.

## Стек

**Языки и фреймворки**
`Python` (asyncio, httpx, Playwright, pytest, Anthropic SDK, Telethon)
`Bash` `PowerShell` `SQL`

**ИБ и методологии**
`OWASP LLM Top 10` `OWASP Top 10` `CVSS 3.1` `MITRE ATT&CK`
`NVD CVE-фид` `PKI` `X.509` `ViPNet` `Coordinator`

**Инфраструктура**
`Linux` `Windows Server` `Docker` `Postgres` `SQLite` `Redis`
`MikroTik` `Cisco` `Zabbix` `Wireshark` `tcpdump`

**AI-стек (Spider)**
`Anthropic API` `OpenAI API` `LangChain` `LlamaIndex` `vector DBs` `RAG`

## Образование

- **МИРЭА** — Российский технологический университет, бакалавр бизнес-информатики (выпуск 2026)
- Подаю документы в магистратуру по информационной безопасности

## Связаться

Открыт к ИБ-позициям в командах, где можно расти через результат.
По коммерческим аудитам — пиши напрямую, обсудим scope и сроки.

- Telegram: [@guttergeishablues](https://t.me/guttergeishablues)
- Email: gasilin-88@mail.ru
- Сайт: [disform.ru](https://disform.ru)
- Телефон: +7 906 743 12 01
