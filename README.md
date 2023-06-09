# Assignment-2.2
For this Assignment, I'm utilising a straightforward Python-Flask application called app.py, which I've hidden behind the HAproxy, a load balancer between the three development servers devA, devB, and devC. A bastion host is established with the intention of serving as the network's main SSH entry point. 

Using city cloud, a total of 5 servers have been deployed. While Dev servers only have private IP addresses, BastionNSO host and HAproxy are given floating IP addresses.

Our flask application is deployed to development servers using ansible-playbook "site.yaml"; to perform load balancing between them, we deploy the haproxy load balancing configuration file.

For testing, all we need to do is curl to the haproxy IP address, and it should respond with the time and hostname of the responding host.
