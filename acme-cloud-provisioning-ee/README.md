# parasol-cloud-provisioning-ee

Cloud infrastructure provisioning EE for AWS, Azure, and GCP

## What's included

### Ansible collections

| Collection | Version | Source |
|---|---|---|
| amazon.aws | - | Private Automation Hub (rh-certified) |
| amazon.ai | - | Private Automation Hub (rh-certified) |
| azure.azcollection | - | Private Automation Hub (rh-certified) |
| google.cloud | - | Private Automation Hub (rh-certified) |



## Details

- **Tags:** `execution-environment`

- **Image registry:** `52.21.70.135/parasol-cloud-provisioning-ee:v1.0.0`

## Use this execution environment

If your EE uses collections from private sources (Automation Hub, private automation hub), update the token settings in `ansible.cfg` before building.


Log in to the registry and pull the image:

```bash
podman login 52.21.70.135
podman pull 52.21.70.135/parasol-cloud-provisioning-ee:v1.0.0
```

If the registry uses a self-signed certificate, you may need to append `--tls-verify=false` to each `podman` command.

To use it in Ansible Automation Platform:

1. Go to **Automation Execution** > **Infrastructure** > **Execution Environments**.
2. Click **Create execution environment** and enter the image URL: `52.21.70.135/parasol-cloud-provisioning-ee:v1.0.0`
3. Select this execution environment in your job templates.

## Build details

- **Base image:** `registry.redhat.io/ansible-automation-platform/ee-minimal-rhel8:2.18`
- **Definition file:** `parasol-cloud-provisioning-ee.yml`
- **Template file:** `parasol-cloud-provisioning-ee-template.yml` - import this into Ansible automation portal to let others create EEs from the same starting point.

To make changes, use this EE's template in Ansible automation portal or rebuild manually with `ansible-builder` and the definition file.
