# grafana-traefik-docker-swarm
#### Grafana with Let's Encrypt in a Docker Swarm


#### Create a secret for storing the password for Grafana database using the command:

<pre><code> printf "YourPassword" | docker secret create grafana-postgres-password - </code></pre> 

#### Create a secret for storing the password for Grafana administrator using the command:

<pre><code>  printf "YourPassword" | docker secret create grafana-application-password -</code></pre> 

#### Create a secret for storing the password for Grafana email account using the command:

<pre><code>   printf "YourPassword" | docker secret create grafana-email-password - </code></pre>

#### Clear passwords from bash history using the command:

<pre><code> history -c && history -w </code></pre>

#### Create a secret for storing the Grafana configuration using the command:

<pre><code> docker secret create ldap.toml /path/to/ldap.toml </code></pre>

#### Deploy Grafana in a Docker Swarm using the command:
<pre><code> docker stack deploy -c grafana.yml grafana </code></pre>