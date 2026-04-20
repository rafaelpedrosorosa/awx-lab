# AWX Lab - Ansible Automation Platform (Open Source)

Laboratório prático utilizando AWX Operator em Kubernetes (Minikube) para automação de tarefas com Ansible.

## Tecnologias
- Kubernetes (Minikube)
- AWX Operator
- Ansible
- Linux

## Objetivo
Simular ambiente enterprise com:
- Inventory
- Projects
- Job Templates
- Execução de playbooks automatizados

## Cenário
- Deploy do AWX em cluster local
- Integração com repositório Git
- Execução de playbooks via interface web

## Exemplo de Playbook
```yaml
- name: Teste AWX
  hosts: all
  become: true
  tasks:
    - name: Criar arquivo
      file:
        path: /tmp/awx-test.txt
        state: touch
