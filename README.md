# ans-hw-01

1. Попробуйте запустить playbook на окружении из test.yml, зафиксируйте значение, которое имеет факт some_fact для указанного хоста при выполнении playbook.

```
TASK [Print fact] **********
ok: [localhost] => {
    "msg": 12
}
```

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на all default fact.

```
TASK [Print fact] ***********
ok: [localhost] => {
    "msg": "all default fact"
}
```