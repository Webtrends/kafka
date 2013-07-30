Description
===========

Installs kafka 0.7.1

Requirements
============
* Java cookbook version >= 1.5
* Runit cookbook

Attributes
==========

* kafka.version - The Kafka version to pull and use
* kafka.install_dir - Location for Kafka to be installed
* kafka.data_dir - Location for Kafka logs
* kafka.log_dir - Location for Kafka log4j logs
* kafka.brokers - An array of the Kafka broker hostnames/fqdn/ips. If this is provided and kafka.broker_id is not we will use this list to generate the id.
* kafka.broker_id - The id of the broker. This must be set to a unique integer for each broker. If not set, it defaults to the machine's ip address without the '.'.
* kafka.broker_host_name - Hostname the broker will advertise to consumers. If not set, kafka will use the host name for the server being deployed to..
* kafka.port - The port the socket server listens on
* kafka.threads - The number of processor threads the socket server uses for receiving and answering requests. If not set, defaults to the number of cores on the machine
* kafka.log_flush_interval - The number of messages to accept before forcing a flush of data to disk
* kafka.log_flush_time_interval - The maximum amount of time (ms) a message can sit in a log before we force a flush
* kafka.log_flush_scheduler_time_interval - The interval (in ms) at which logs are checked to see if they need to be flushed to disk
* kafka.log_retention_hours - The minimum age of a log file to be eligible for deletion

Usage
=====

* kafka - Install a Kafka broker.

= LICENSE and AUTHOR:

Author:: Ivan von Nagy ()

Copyright:: 2012, Webtrends, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.