# docker-selenium-grid-hub

Setup a Selenium Grid Hub in a docker container. You can access the Hub's console at an address 
similar to this: http://selenhub.COMPANY.com:4444

The publish port will be 4442, the subscribe port will be 4443, and the http port will be 4444.

https://github.com/SeleniumHQ/docker-selenium

For information about PTA and how to use it with this Ansible role please visit https://github.com/Forcepoint/fp-pta-overview/blob/master/README.md

## Requirements

The host is already configured as a docker host.

## Role Variables

### REQUIRED

* docker_selenium_grib_hub_host_dns: The DNS/IP of the system running this container.

### OPTIONAL

* docker_selenium_grid_hub_version: The version of the selenium grid to use.
* docker_selenium_grid_hub_restart_always: If yes, restart the OS when applying this role. Defaults to no.
  This is useful if you fear that the grid is having longevity problems.

## Dependencies

None

## Example Playbook

    - hosts: servers
      vars:
        docker_selenium_grid_hub_version: "latest"
        docker_selenium_grid_hub_restart_always: yes
      roles:
         - role: docker-selenium-grid-hub

## License

BSD-3-Clause

## Author Information

Jeremy Cornett <jeremy.cornett@forcepoint.com>
