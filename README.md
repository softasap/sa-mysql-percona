sa-mysql-percona
================

[![Build Status](https://travis-ci.org/softasap/sa-mysql-percona.svg?branch=master)](https://travis-ci.org/softasap/sa-mysql-percona)

Drop-in sa-mysql compatible repository that installs Percona Server for MySQL - a free, fully compatible, enhanced, 
open source drop-in replacement for MySQL that provides superior performance, scalability and instrumentation.

Example of usage (all parameters are optional)

Simple

```YAML
  roles:
    - {
        role: "sa-mysql-percona"
      }
```

Advanced:


```YAML

  roles:
    - {
        role: "sa-mysql-percona",
        mysql_root_user: root,
        mysql_root_password: devroot,
      - mysql_databases:
        - name: app_db
          encoding: utf8
          collation: utf8_general_ci
      - mysql_users:
        - name: app_user
          host: "%"
          password: dYud8LHBBptGN96LSn0e
          priv: "app_db.*:ALL"
      }

```


Usage with ansible galaxy workflow
----------------------------------

If you installed the sa-mysql-percona role using the command


`
   ansible-galaxy install softasap.sa-mysql-percona
`

the role will be available in the folder library/softasap.sa-mysql-percona
Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa-mysql-percona"
       }

```




Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)
