# JSNAPY EXAMPLE: VALIDATE FIREWALL POLICY COUNTERS

This example will show how to use JSNAPY to make sure the expected firewall policy counters are being received

## To run the playbook

Two options provided:

### Dockerfile

1. build the container image with

```sh
make container
```

2. run the playbook within the container

```sh
make ansible
```

### Your own Python environment

1. install python dependencies 

```sh
pip install -r docker/requirements.txt
```

2. change into Ansible directory 

```
cd ansible
```

3. install Juniper Ansible modules 

```sh
ansible-galaxy install juniper.junos
```

4. type 

```sh
ansible-playbook pb.jsnapy.firewall.counter.yaml
```

## Dependencies

Official Juniper Ansible modules

```sh
ansible-galaxy install juniper.junos
```

## How it works

The playbook works like this:

- We will be requesting the firewall security policy counters
- The output will be stored as an object called `test_firewall`
- We assert the pass/fail within the playbook

## examples screenshot
![ansible-playbook pb.jsnapy.firewall.counter.yaml](./static/images/screenshot.png)
