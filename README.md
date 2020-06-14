# ansible-role-docker-gitlab

This role runs gitlab community edition with [Let's Encrypt](https://letsencrypt.org/) behind a traefik reverse proxy. It is intended to work with [ansible-role-docker-traefik](https://github.com/mambord/ansible-role-docker-traefik).


## Defaults

These are the default values for this playbook.

```yaml
# gitlab settings
docker_gitlab_image_tag: latest
docker_gitlab_url: gitlab.local
docker_gitlab_host_ssh_port: 22
docker_gitlab_conf_smtp_enable: "false"

# traefik network
docker_gitlab_traefik_network: traefik

# place for configs and data
docker_gitlab_base_dir: /opt/gitlab
```

If ```docker_gitlab_conf_smtp_enable: "true"```, the following options are available:

```yaml
# gitlab_rails['smtp_address']
docker_gitlab_conf_smtp_address:

# gitlab_rails['smtp_port']
docker_gitlab_conf_smtp_port:

# gitlab_rails['smtp_user_name']
docker_gitlab_conf_smtp_user_name:

# gitlab_rails['smtp_password']
docker_gitlab_conf_smtp_password:

# gitlab_rails['smtp_domain']
docker_gitlab_conf_smtp_domain:

# gitlab_rails['smtp_authentication']
docker_gitlab_conf_smtp_authentication:

# gitlab_rails['smtp_enable_starttls_auto']
docker_gitlab_conf_smtp_enable_starttls_auto:

# gitlab_rails['smtp_tls']
docker_gitlab_conf_smtp_tls:

# gitlab_rails['gitlab_email_from']
docker_gitlab_conf_smtp_email_from:
```

## File tree
```
/opt/gitlab
    ├── config
    ├── logs
    ├── data
    └── docker-compose.yml
```
