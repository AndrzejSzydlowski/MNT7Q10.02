# Домашнее задание к занятию "10.02. Системы мониторинга"

## 1.Опишите основные плюсы и минусы pull и push систем мониторинга.
- Push модель работает посредством udp и имплицирует на себя минусы и плюсы udp (это скорость, и возможная потеря пакетов) также можно настроить на агенте направление поставки метрик, больше подходит для логов в реальном времени
- Pull модель гарантирует достоверность данных, агент локально опрашивает метрики на системе и записывает в локальный лог, в определенный промежуток времени приходит мастер агент и забирает эти логи, больше подходит для статистического ведения логов, более медленая модель, но более безопасная.
## 2.Какие из ниже перечисленных систем относятся к push модели, а какие к pull? А может есть гибридные?
- Prometheus pull
- Tick push 
- Zabbix both
- VictoriaMetrics both
- Nagios push

## 3.Склонируйте себе репозиторий и запустите TICK-стэк, используя технологии docker и docker-compose.

┌──(rimm㉿FR-KL)-[~/dockerfolders/TICK/TICK-docker/1.3]
└─$ curl http://localhost:8086/ping

┌──(rimm㉿FR-KL)-[~/dockerfolders/TICK/TICK-docker/1.3]
└─$ curl http://localhost:8888
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="Content-type" content="text/html; charset=utf-8"/>
    <title>Chronograf</title>
  <link rel="shortcut icon" href="/favicon.ico"><link href="/chronograf.css" rel="stylesheet"></head>
  <body>
    <div id='react-root' data-basepath=""></div>
  <script type="text/javascript" src="/manifest.0b50876f6444e513725c.js"></script><script type="text/javascript" src="/vendor.36ee797884f822b1fbde.js"></script><script type="text/javascript" src="/app.3eec41dc0f57667d6ff4.js"></script></body>
</html>

┌──(rimm㉿FR-KL)-[~/dockerfolders/TICK/TICK-docker/1.3]
└─$ curl http://localhost:9092/kapacitor/v1/ping
