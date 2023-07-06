
```
ansible-inventory -i hosts_01  --graph
@all:
  |--@demo:
  |  |--192.168.33.11
  |  |--192.168.33.12
  |--@ungrouped:
```



```
ansible-inventory -i hosts_03 --graph
@all:
  |--@backend:
  |  |--192.168.33.12
  |--@frontend:
  |  |--192.168.33.11
  |--@ungrouped:
```
