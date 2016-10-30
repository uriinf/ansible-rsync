# Ansible playbook to sync data to remote host[s] via docker container on destination side.
Runs rsyncd container on remote host and sync data.
## Example:
```sh
ansible-playbook -i static.hosts deploy-static.yml
```
It will sync current directory to destination_host:/tmp/rsync
### Playbook requirements:
* dst_host (rsync data to)
 * docker and docker-py installed and running
 * user deploy with permissions to run docker and modify iptables with sudo
