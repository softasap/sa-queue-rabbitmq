sa-queue-rabbitmq
=================

[![Build Status](https://travis-ci.org/softasap/sa-queue-rabbitmq.svg?branch=master)](https://travis-ci.org/softasap/sa-queue-rabbitmq)

rabbitmq_properties: list of regexes in form (regexp, line) to adjust conf  /etc/rabbitmq/rabbitmq.config file with necessary changes



Example of usage (all parameters are optional)

Simple

  roles:
    - {
        role: "sa-queue-rabbitmq"
      }


Advanced:


  roles:
    - {
        role: "sa-queue-rabbitmq",
        rabbitmq_version: 3.6.1  
        rabbitmq_properties:
          - {regexp: "^default_user .*", line: "default_user myuser"}
	  - {regexp: "^default_pass .*", line: "default_pass dsfgdsgdfsgsg"}

      }



