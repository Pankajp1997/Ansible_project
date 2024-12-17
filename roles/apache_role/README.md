# Apache Role

This Ansible role installs, configures, and deploys the Apache HTTP Server on Linux systems.

## Role Variables:
| Variable         | Default Value      | Description                       |
|------------------|--------------------|-----------------------------------|
| `apache_package` | `httpd`           | Apache package name               |
| `apache_service` | `httpd`           | Apache service name               |
| `apache_port`    | `80`              | Port for Apache to listen         |
| `document_root`  | `/var/www/html`   | Document root for web content     |
| `server_name`    | `localhost`       | Server name                       |

## Example Playbook:

```yaml
- name: Deploy Apache Web Server
  hosts: web_servers
  roles:
    - apache_role

---

### **How to Run the Project**  

1. **Prepare the Inventory File** (`inventory`) with the target servers and credentials.  
2. **Run the Playbook**:

```bash
ansible-playbook -i inventory playbook.yml
