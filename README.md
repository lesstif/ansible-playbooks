# ansible-playbooks
앤서블 플레이북과 recipe

# install

```sh
ansible-galaxy install -r roles/requirements.yml 
```

# 실행

```sh
ansible-playbook -i inventory increase-open-filemax.yml
```
