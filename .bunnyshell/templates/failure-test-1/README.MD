Template that will fail during the create environment from template flow.

Expected error:
```: Failed to compile the value "cat << EOF > my_values.yaml
    serviceImage: {{ components.api-image.image }}
    replicas: 1
    ingress:
        className: bns-nginx
        host: api-{{ env.base_domain }}
    postgres:
        host: '{{ components.postgres.exported.POSTGRES_HOSdT }}'
        db: '{{ env.vars.POSTGRES_DB }}'
        user: '{{ env.vars.POSTGRES_USER }}'
        password: '{{ env.vars.POSTGRES_PASSWORD }}'
    frontendUrl: '{{ env.vars.FRONTEND_URL }}'
EOF
": Key "POSTGRES_HOSdT" for array with keys "POSTGRES_HOST" does not exist.```
