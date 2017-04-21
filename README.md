## OracleJDK [![Build Status](https://travis-ci.org/fabiohbarbosa/oracle-jdk.png)](https://travis-ci.org/fabiohbarbosa/oracle-jdk)


Forked: [ANXS.oracle-jdk](https://github.com/ANXS/oracle-jdk). Motivation: keep the ansible role up to date and making improvements.


Ansible role to install the latest update of Oracle/Sun JDK version(s).


#### Requirements & Dependencies
- Tested on Ansible 2.0 or higher


#### Variables

```yaml
oracle_jdk_java_versions: [8]             # A list of java versions you want to have installed (6, 7, 8 and/or 9)
oracle_jdk_java_version_default: 8        # The java version you want to be the system default
```


#### In operation

To switch between different Java versions, you could use the following terminal command:
```bash
sudo update-alternatives --config java
```


#### Example Playbook

```yaml
  roles:
    - { role: fabiohbarbosa.oracle-jdk, oracle_jdk_java_versions: [6,7,8,9], oracle_jdk_java_version_default: 8 }
```


#### Testing
This project comes with a VagrantFile, this is a fast and easy way to test changes to the role, fire it up with `vagrant up`

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with vagrant


#### License

Licensed under the MIT License. See the LICENSE file for details.


#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/fabiohbarbosa/oracle-jdk/issues)!
