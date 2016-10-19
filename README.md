# How to append to a list in Ansible

In this repository you can find examples of how to append things to lists in Ansible.

## How to run demonstration
`ansible-playbook demo-append-list.yml`

## Example output
```shell

max@max-x1:~/work/ansible-append-list$ ansible-playbook demo-append-list.yml 
 [WARNING]: provided hosts list is empty, only localhost is available

statically included: /home/max/work/ansible-append-list/tasks/append-list-to-list.yml
statically included: /home/max/work/ansible-append-list/tasks/append-list-of-map-to-list.yml
statically included: /home/max/work/ansible-append-list/tasks/append-integer-to-list.yml
statically included: /home/max/work/ansible-append-list/tasks/append-boolean-to-list.yml
statically included: /home/max/work/ansible-append-list/tasks/append-string-to-list.yml

PLAY [localhost] ***************************************************************

TASK [setup] *******************************************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "msg": "Append list to list, or merge two lists"
}

TASK [Setup two lists to be merged] ********************************************
ok: [localhost]

TASK [Merge the two lists] *****************************************************
ok: [localhost]

TASK [Demonstrate merged lists] ************************************************
ok: [localhost] => {
    "lists_merged": [
        1, 
        2, 
        3, 
        4, 
        5, 
        6
    ]
}

TASK [debug] *******************************************************************
ok: [localhost] => {
    "msg": "Append/merge list of maps to list"
}

TASK [Setup two lists to be merged] ********************************************
ok: [localhost]

TASK [Merge the two lists of maps] *********************************************
ok: [localhost]

TASK [Demonstrate merged lists] ************************************************
ok: [localhost] => {
    "lists_merged": [
        {
            "first_name": "John", 
            "last_name": "Doe"
        }, 
        {
            "first_name": "Jane", 
            "last_name": "Doe"
        }, 
        {
            "first_name": "Douglas", 
            "last_name": "Adams"
        }, 
        {
            "first_name": "Frederic", 
            "last_name": "Bastiat"
        }
    ]
}

TASK [Initialize an empty list] ************************************************
ok: [localhost]

TASK [Setup a integer variable] ************************************************
ok: [localhost]

TASK [Append item to list] *****************************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "the_list": [
        5
    ]
}

TASK [Append another item to the list] *****************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "the_list": [
        5, 
        6
    ]
}

TASK [Initialize an empty list for our truths] *********************************
ok: [localhost]

TASK [Setup a boolean variable] ************************************************
ok: [localhost]

TASK [Append boolean to list] **************************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "my_thruths": [
        true
    ]
}

TASK [Append another boolean to the list] **************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "my_thruths": [
        true, 
        false
    ]
}

TASK [Initialize an empty list for our strings] ********************************
ok: [localhost]

TASK [Setup a string variable] *************************************************
ok: [localhost]

TASK [Append string to list] ***************************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "my_strings": [
        "Max"
    ]
}

TASK [Append another item to the list] *****************************************
ok: [localhost]

TASK [debug] *******************************************************************
ok: [localhost] => {
    "my_strings": [
        "Max", 
        "Power"
    ]
}

PLAY RECAP *********************************************************************
localhost                  : ok=27   changed=0    unreachable=0    failed=0   

```

