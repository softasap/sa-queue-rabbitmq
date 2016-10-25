sa-queue-rabbitmq
=================

[![Build Status](https://travis-ci.org/softasap/sa-queue-rabbitmq.svg?branch=master)](https://travis-ci.org/softasap/sa-queue-rabbitmq)

rabbitmq_properties: list of regexes in form (regexp, line) to adjust conf  /etc/rabbitmq/rabbitmq.config file with necessary changes



Example of usage (all parameters are optional)

Simple
```
  roles:
    - {
        role: "sa-queue-rabbitmq"
      }
```

Advanced:

Watchout for commas in rabbitmq_properties !

```
  roles:
    - {
        role: "sa-queue-rabbitmq",
        rabbitmq_version: 3.6.1  
        rabbitmq_properties:
          - {regexp: "^%% {default_user, .*", line: "{default_user,        <<"guest">>}"}
      	  - {regexp: "^%% {default_pass, .*", line: "{default_pass,        <<"guest">>},"}

      }
```


Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

