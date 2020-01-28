# docker-selenium-grid-hub

Setup a Selenium Grid Hub in a docker container. You can access the Hub's console at an address similar to this: http://selenhub.COMPANY.com:4444/grid/console

## Requirements

None

## Role Variables

### REQUIRED

* docker_selenium_grid_hub_dns: The DNS name to assign to the hub. EX: selenhub.COMPANY.com
* docker_selenium_grid_hub_port: The port to assign to the hub. EX: 4444

### OPTIONAL

* docker_selenium_grid_hub_version: The version of the selenium grid to use.
* docker_selenium_grid_hub_container_name: The name to give the Hub container.
* docker_selenium_grid_hub_project_name: The name to give the docker compose project.
* docker_selenium_grid_hub_restart_always: If yes, restart the OS when applying this role. Defaults to no.
  This is useful if you fear that the grid is having longevity problems.

## Dependencies

None

## Example Playbook

    - hosts: servers
      vars:
        docker_selenium_grid_hub_dns: selenhub.COMPANY.com
        docker_selenium_grid_hub_port: 4444
      roles:
         - role: docker-selenium-grid-hub

## License

BSD

## Author Information

Jeremy Cornett <jeremy.cornett@forcepoint.com>
