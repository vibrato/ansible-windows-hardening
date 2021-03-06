# windows-hardening (Ansible Role)

[![Build Status](http://img.shields.io/travis/dev-sec/ansible-windows-hardening.svg)][1]
[![Gitter Chat](https://badges.gitter.im/Join%20Chat.svg)][2]
[![Ansible Galaxy]()][3]

## Description

This roles provides a role for ensuring that a Windows 2012 R2 system is compliant with the [DevSec Windows Baseline](https://github.com/dev-sec/windows-baseline).

## Requirements

* Ansible 2.3.0

## Variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| TBD            |               |                                    |

## Example Playbook

    - hosts: localhost
      roles:
        - dev-sec.windows-hardening

## Local Testing


For all our tests we use `test-kitchen`. If you are not familiar with `test-kitchen` please have a look at [their guide](http://kitchen.ci/docs/getting-started).

We create multiple hosts - one linux host where Ansible runs on and the Windows hosts.

Next install test-kitchen:

```bash
# Install dependencies
gem install bundler
bundle install
```

Then you can run the playbook and tests:
```
# create the ansible and windows hosts
bundle exec kitchen create

# run ansible playbook on windows host
bundle exec kitchen converge default-ansibleserver

# verify windows machines
bundle exec kitchen verify windows

```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License and Author

* Author:: Sebastian Gumprich <sebastian.gumprich@38.de>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


[1]: http://travis-ci.org/dev-sec/ansible-os-hardening
[2]: https://gitter.im/dev-sec/general
[3]: https://galaxy.ansible.com/dev-sec/os-hardening
