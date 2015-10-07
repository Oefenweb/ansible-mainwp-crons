## mainwp-crons

[![Build Status](https://travis-ci.org/Oefenweb/ansible-mainwp-crons.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-mainwp-crons) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-mainwp--crons-blue.svg)](https://galaxy.ansible.com/list#/roles/5399)

Manage [cron jobs](http://docs.mainwp.com/disable-wp-cron/) related to [MainWP](https://mainwp.com/).

#### Requirements

None

#### Variables

* `mainwp_crons_sites` [default: `[]`]: A list of MainWP sites
* `mainwp_crons_sites.{n}.name` [required]: Name of the site
* `mainwp_crons_sites.{n}.url` [required]: Url of the site
* `mainwp_crons_sites.{n}.state`: [default: `present`]: Whether to ensure the job is present or absent

## Dependencies

None

#### Example(s)

##### Simple configuration

```yaml
---
- hosts: all
  roles:
    - mainwp-crons
  vars:
    mainwp_crons_sites:
      - name: site
        url: http://localhost
```

#### License

MIT

#### Author Information

* Mark van Driel
* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-mainwp-crons/issues)!
