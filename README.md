# cassandra-datastax-agent

This image adds the [DataStax agent](http://docs.datastax.com/en/opscenter/5.2/opsc/install/installingAgents.html) to the [official Cassandra 2.1](https://hub.docker.com/_/cassandra/) image so that that the Node/Cluster can be monitored.

# Usage

Add the *OPS_IP* as an environment variable to the *docker run* command. The value of this variable is the IP address where [OpsCenter](http://docs.datastax.com/en/opscenter/5.2/opsc/about_c.html) is running. So assuming OpsCenter is running at IP 42.42.42.42, you need to launch the container with:

    docker run --name cassandra-node -P -e OPS_IP=42.42.42.42  yoanisgil/cassandra-datastax-agent:2.1

Same environment variables, volumes, ports, etc from the official Cassandra image applies.
