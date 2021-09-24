# ansible-playbooks
앤서블 플레이북과 recipe

## install

```sh
ansible-galaxy install -r roles/requirements.yml 
```

## 실행

```sh
ansible-playbook -i inventory increase-open-filemax.yml
```

## playbook list

### add-users-to-sudoers

become method 가 su 이므로 **-K, --ask-become-pass** 옵션 사용

```sh
ansible-playbook -i inventory add-users-to-sudoers.yml -K
```

다른 사용자를 추가할 경우 users.json에 추가할 사용자를 배열로 기술하고 playbook 실행

```json
{
    "users": [
        "user1",
        "user2"
    ]
}
```

```sh
ansible-playbook -i inventory add-users-to-sudoers.yml -K -e '@users.json'
```

### install-dotfiles

github 에 있는 dotfiles 을 설치

```sh
ansible-playbook -i inventory install-dotfiles.yml
```
