# Ansible-Naiveproy

This ansible playbook automatically deploys [Naiveproxy](https://github.com/klzgrad/naiveproxy) on your Linux server/VPS.

# Usage

1. Install Ansible on your Linux server/VPS

````shell
# you can
# Install on Debian:
sudo apt install ansible

or

# Install on Centos:
sudo yum install ansible

or

# Install by pip
python3 -m pip install --user ansible
````
for more infomation about install ansible, please check [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html)


2. Enable DNS resolution for your server/VPS

* add A (IPv4) or AAAA (IPv6) records in your Domain DNS management interface with the server/VPS IP addresses.


3. Clone this project and apply ansible playbook on your server/VPS

```shell
git clone https://github.com/5uy4n9/ansible-naiveproxy.git

cd ansible-naiveproxy

# replace "example.com" to your domain, replace "ssl@example.com" to your personal Email, replace "foo" to your username, replace "bar" to your password
sudo ansible-playbook naiveproxy.yml -e "domain_name=example.com email_address=ssl@example.com username=foo password=bar"
```


4. Client Usage

* For Windows, Linux, Mac OS, and OpenWrt, Download [Client](https://github.com/klzgrad/naiveproxy/releases/latest/) and run with [config](https://github.com/klzgrad/naiveproxy#client-setup)

* For iOS, you can use [Shadowrocket](https://apps.apple.com/us/app/shadowrocket/id932747118), add HTTP2 proxy with service info

* For Android, you can use ([NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid) with [naive-plugin](https://github.com/SagerNet/SagerNet/releases)), add Naive protocol with service info