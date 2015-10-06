## mainwp-crons

[![Build Status](https://travis-ci.org/Oefenweb/ansible-mainwp-crons.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-mainwp-crons)

Manage MainWP cronjobs in Debian-like systems.

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
