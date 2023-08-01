# Ansible

An imperative infrastructure as code tool for configuration management and orchestration of your infrastructure  

**_Uses_**:

- Install software
- Configure all services
- Test your servers
- Deploy application
- Many more...

## Key Terms

### Imperative tool

Tool where you define the steps to execute in order to reach the desired state/solution.  
\*\*\*\*\*\*\*\*\*\*

### Playbook

Definition and example  
\*\*\*\*\*\*\*\*\*\*

### Roles

Reusable set of tasks. Kept in it's own roles directory. 
*_tags_*  
Label or identify a task with selective way to run specific tasks or groups of tasks in a playbook  

```yaml
- name: <task_that_does_x>
  <module>:
    <parameter>: <info>
  tags: [<tag1>, <tag2>]
```  

\*\*\*\*\*\*\*\*\*\*

### Tasks

Definition and example  
\*\*\*\*\*\*\*\*\*\*

### Templates

Simple text files that use Jinja2 templating engine
\*\*\*\*\*\*\*\*\*\*

### Handlers

Special tasks that are executed only when specific events trigger them. Usually used to respond to changes in the system state, such as config updates or service restarts.

```yaml
- name: <task_that_does_x>
  <module>:
    <parameter>: <info>
  notify: <Handler_name>
```

### Defaults

Variables. It's own defaults directory within the role. Good practice is to prefix variable name with role name. Values can be number, string(Quotes around strings can be omitted), list etc.  

```yaml
<role_str_variable>: <value>
<role_list_variable>:
 - <str>
 - <str>
<role_int_variable>: 80
```

In order to use variable in task you need to wrap them into double curly brackets {{}} and quotes "".  

```yaml
- name: <task_that_does_x>
  <module>:
    <parameter>: "{{ <variable_name> }}"
```

Can override a default variable by specifying in the task

```yaml
- name: <task_that_does_x>
  <roles>:
    <parameter>: "{{ <variable_name> }}"
  vars:
   <default_var_name>: <new value>
```

\*\*\*\*\*\*\*\*\*\*

### Lists and loops

Combining tasks together

```yaml
- name: <task_that_does_x>
  <module>:
    <parameter>: "{{ item }}"
  with_items:
   - <item1>
   - <item2>
  tags: [<tag>]
```

or pass from defaults  

```yaml
- name: <task_that_does_x>
  <module>:
    <parameter>: "{{ item }}"
  with_items: "{{ <role_default_variable> }}"
  tags: [<tag>]
```


\*\*\*\*\*\*\*\*\*\*

---

## GETTING STARTED COMMANDS

### Ping hosts in host file

`ansible <host group> -m ping -i ./hosts`  
`-m <module>` loads module  
`-i </path/to/inventory>` inventory  
`--tags="<tag1>,<tag2>"` Run only tasks with specific tags  
`-vvvv` Verbosity level 4 more `v`'s more verbose  

\*\*\*\*\*\*\*\*\*\*

### Run ansible playbook

`ansible-playbook -i </path/to/hosts> <path/to/playbook.yml>`  
`-i </path/to/inventory>` inventory  

\*\*\*\*\*\*\*\*\*\*

### COMMAND

``  
`-`

\*\*\*\*\*\*\*\*\*\*

---

## ADVANCED COMMANDS

### COMMAND

``  
`-`

\*\*\*\*\*\*\*\*\*\*

### COMMAND

``  
`-`

\*\*\*\*\*\*\*\*\*\*

---

## Configs

### Project Structure

```text
my_playbook/
├── playbook.yml
├── tasks/
│   ├── task_file_1.yml
│   ├── task_file_2.yml
│   └── task_file_3.yml
└── roles/
    └── my_role/
        ├── tasks/
        │   ├── main.yml
        │   ├── additional_tasks.yml
        │   └── more_tasks.yml
        └── templates /
        │   └── template.conf.j2
        └── defaults /
        │   └── main.yml
```

### Inventory file

`hosts.yaml`
What does the config do  
Config example and definition of each term 

### Roles

`main.yaml`

`task1.yaml`

```yaml
- name: <descriptive_name>
  <ansible_module>:
    <module_parameter>: epel-release
    <module_parameter>: present
  tags: [nginx]
```

```yaml
- name: install epel
  yum:
    name: epel-release
    state: present
  tags: [nginx]

- name: install nginx
  yum:
    name: nginx
    state: present
  tags: [nginx]
```

### Playbook file

`playbook.yaml`
What does the config do  
Config example and definition of each term

```yaml
- hosts: ansible_tutorial
  become: yes
  become_user: root
  roles:
   - nginx
```

```yaml
- hosts: <hosts or groups from inventory file>
  become: <privileges escalation>
  become_user: <become privileged user>
  roles: 
   - <list of roles that will apply to our servers>
```

\*\*\*\*\*\*\*\*\*\*

---

## Processes

### Process

1. steps
2. step
3. step

\*\*\*\*\*\*\*\*\*\*

---

## Links

[Ansible Modules](http://docs.ansible.com/ansible/modules_by_category.html)  
[Tutorial](https://github.com/blacksaildivision/ansible-tutorial/tree/ab75bfd43512e68c4b961111f8f4e6abf8e761e5)  
