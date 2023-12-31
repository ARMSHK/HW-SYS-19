# Домашнее задание к занятию «Кластеризация и балансировка нагрузки» - Romashkova Alina

### Задание 1
- Запустите два simple python сервера на своей виртуальной машине на разных портах
- Установите и настройте HAProxy, воспользуйтесь материалами к лекции по [ссылке](2/)
- Настройте балансировку Round-robin на 4 уровне.
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.


### Задание 2
- Запустите три simple python сервера на своей виртуальной машине на разных портах
- Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
- HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.


#### Результат к заданию 1 и 2

- Запуск 2 Simple Python Server (s1 :8888, s2 :9999, s3 :8500 - добавиться позже на скриншотах)

![Curl_H_Host](https://github.com/ARMSHK/HW-SYS-19/blob/main/img/Curl_H_Host_8888_9999.png)

- Haproxy перенаправление на s1, s2, s3 (curl http://127.0.0.1:8080)

![Haproxy_web](https://github.com/ARMSHK/HW-SYS-19/blob/main/img/Haproxy_web.png)

- ссылка на [Haproxy.cfg](https://github.com/ARMSHK/HW-SYS-19/blob/main/cfgs/haproxy.cfg)
- Haproxy + example (curl -H 'Host: example-http.com' http://127.0.0.1)

![Haproxy_example](https://github.com/ARMSHK/HW-SYS-19/blob/main/img/Haproxy%20%2B%20example.png)
