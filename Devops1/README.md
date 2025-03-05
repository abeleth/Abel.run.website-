<details>
  <summary>What is DevOps?</summary>

"From Amazon's standpoint, DevOps is a set of practices and cultural philosophies that enables organizations to improve collaboration between development and operations teams to automate and streamline the process of software development, deployment, and infrastructure management. At Amazon, DevOps is a key enabler of continuous innovation, allowing for faster delivery of applications, improvements, and services with a focus on customer satisfaction. Amazon emphasizes the use of AWS tools and services to automate infrastructure provisioning, continuous integration and delivery (CI/CD), and monitoring, fostering a rapid feedback loop to detect and resolve issues quickly. This approach enables teams to release software updates quickly, efficiently, and securely, maintaining high availability and reliability in a dynamic, cloud-based environment. Through practices like Infrastructure as Code (IaC) and automated testing, Amazon's DevOps culture aims to enhance operational efficiency, reduce downtime, and ensure that software aligns with customer needs and business objectives."

</details>

<details>
  <summary>In DevOps what is expecting on achieving in the process?</summary>


**Faster Time to Market:** By automating manual processes and integrating development with operations, DevOps enables rapid delivery of software features, updates, and fixes, reducing the time between writing code and making it available to users.

**Improved Collaboration:** DevOps breaks down silos between development, operations, and other teams, fostering a culture of shared responsibility, communication, and collaboration.

**Continuous Integration and Continuous Delivery (CI/CD):** DevOps enables automated and continuous testing, integration, and delivery of code, ensuring that changes are deployed more frequently and reliably.

**Increased Efficiency and Automation:** By automating repetitive tasks such as testing, infrastructure provisioning, and deployment, DevOps helps reduce human error, increase productivity, and free up resources for higher-value tasks.

**Higher Quality and Reliability:** Through automated testing, monitoring, and feedback loops, DevOps ensures that software is of higher quality, with fewer bugs and vulnerabilities. Continuous monitoring allows for early detection and resolution of issues.

**Scalability and Flexibility:** DevOps practices, especially in cloud environments, enable teams to scale applications and infrastructure dynamically in response to changing business needs, traffic, and demand.

**Faster Incident Response and Recovery:** DevOps encourages continuous monitoring, quick issue detection, and rapid response to incidents, enabling teams to minimize downtime and recover from failures faster.

**Cost Efficiency:** Through automation and optimized infrastructure management (e.g., Infrastructure as Code), DevOps reduces operational costs by improving resource utilization and minimizing manual intervention.

**Security and Compliance:** DevOps incorporates security practices early in the development process (often called DevSecOps), ensuring that security is integrated into the pipeline, rather than being an afterthought.

</details>


<details>
  <summary>To be a successfil DevOps Engineer you neen this skills.</summary>



**Technical Skills:**

Cloud Computing (AWS, Google Cloud, Azure)

Automation & Configuration Management (Terraform, Ansible, Chef, Puppet)

CI/CD Tools (Jenkins, GitLab CI, CircleCI)

Containerization & Orchestration (Docker, Kubernetes)

Scripting & Programming (Python, Bash, Ruby)

Monitoring & Logging (Prometheus, Grafana, ELK Stack)

Version Control (Git)

**Soft Skills:**

Collaboration & Communication

Problem-Solving

Adaptability & Continuous Learning

Time Management

**DevOps Culture & Principles:**

Agile Mindset

Infrastructure as Code (IaC)

Continuous Improvement

Collaboration & Shared Responsibility

**Security (DevSecOps):**

Knowledge of integrating security in the development process.

**Experience:**

Hands-on experience in real-world projects and environments.

**Certifications (Optional but Beneficial):**

AWS, Google Cloud, Azure DevOps, Kubernetes, Docker, Terraform certifications.

</details>
# Installation

# Git on **Linux Ubuntu**

![image](https://github.com/user-attachments/assets/8cb13eff-5d97-4035-9078-4d0352bb5652)


```yaml
sudo apt update && sudo apt install -y git
git --version

```

# AWS on **Linux Ubuntu**


![image](https://github.com/user-attachments/assets/0efdc521-0da6-40db-8568-c69133cb601b)

```yaml
aws --version
sudo apt  install awscli
aws --version

```

# Docker on **Linux Ubuntu**
![image](https://github.com/user-attachments/assets/4f4e97c3-2bf6-4b64-9d70-acf94a8fd93c)



```yaml
sudo apt update
sudo apt install -y [docker.io](http://docker.io/)
sudo systemctl start docker
sudo systemctl enable docker
docker --version
```

docker login faild errorr on jenkins

```yaml
sudo su
sudo usermod -aG docker jenkins
sudo systemctl restart jenkins
```

# Java on **Linux Ubuntu**


![image](https://github.com/user-attachments/assets/d0c3a526-91c2-4a6f-a57e-38b10f5665cf)

```yaml
java -version
sudo apt install openjdk-21-jre-headless
java -version
```

# Python on **Linux Ubuntu**


![image](https://github.com/user-attachments/assets/cb67e341-2d4b-4ab8-8af8-9a951c946922)

```yaml
sudo apt update && sudo apt install -y python3 python3-pip python3-venv
python3 --version
sudo apt install python3-pip
pip3 --version

```

### **Verify Installation:**

Run these commands to check if the tools are installed properly:

```yaml
git --version
docker --version
terraform --version
aws --version
kubectl version --client
```

# Jenkins on **Linux Ubuntu**


![image](https://github.com/user-attachments/assets/c08d9b8c-a3a6-4ffb-94dd-dce94f4fb926)

```yaml
sudo apt update
sudo apt install openjdk-21-jdk
java -version
sudo apt update
sudo systemctl start jenkins
cat /Users/$(whoami)/. jenkins/secrets/initialAdminPassword
```

password→

> [http://localhost:](http://localhost/) or IP 8080
> 

# **Install Jenkins for Automation:**

- Install Jenkins on the EC2 instance to automate deployment: Install Java

```
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.8" 2023-07-18
OpenJDK Runtime Environment (build 17.0.8+7-Debian-1deb12u1)
OpenJDK 64-Bit Server VM (build 17.0.8+7-Debian-1deb12u1, mixed mode, sharing)

#jenkins
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

```yaml
sudo service jenkins status
```

- Access Jenkins in a web browser using the public IP of your EC2 instance.
    
    publicIp:8080
    

sudo cat   `/var/lib/jenkins/secrets/initialAdminPassword`

cat /Users/$(whoami)/. jenkins/secrets/initialAdminPassword

 **Monitoring**

# **Install Prometheus and Grafana:**

![image](https://github.com/user-attachments/assets/92f0e6ef-cc65-4525-894e-49645ab8fa35)

Set up Prometheus and Grafana to monitor your application.

**Installing Prometheus:**

First, create a dedicated Linux user for Prometheus and download Prometheus:

```
sudo useradd --system --no-create-home --shell /bin/false prometheus
wget https://github.com/prometheus/prometheus/releases/download/v2.47.1/prometheus-2.47.1.linux-amd64.tar.gz
```

Extract Prometheus files, move them, and create directories:

```
tar -xvf prometheus-2.47.1.linux-amd64.tar.gz
cd prometheus-2.47.1.linux-amd64/
sudo mkdir -p /data /etc/prometheus
sudo mv prometheus promtool /usr/local/bin/
sudo mv consoles/ console_libraries/ /etc/prometheus/
sudo mv prometheus.yml /etc/prometheus/prometheus.yml
```

Set ownership for directories:

```
sudo chown -R prometheus:prometheus /etc/prometheus/ /data/
```

Create a systemd unit configuration file for Prometheus:

```
sudo nano /etc/systemd/system/prometheus.service
```

Add the following content to the `prometheus.service` file:

```
[Unit]
Description=Prometheus
Wants=network-online.target
After=network-online.target

StartLimitIntervalSec=500
StartLimitBurst=5

[Service]
User=prometheus
Group=prometheus
Type=simple
Restart=on-failure
RestartSec=5s
ExecStart=/usr/local/bin/prometheus \
  --config.file=/etc/prometheus/prometheus.yml \
  --storage.tsdb.path=/data \
  --web.console.templates=/etc/prometheus/consoles \
  --web.console.libraries=/etc/prometheus/console_libraries \
  --web.listen-address=0.0.0.0:9090 \
  --web.enable-lifecycle

[Install]
WantedBy=multi-user.target

```

Verify Prometheus's status:

```
sudo systemctl enable prometheus
sudo systemctl start prometheus
```

```
sudo systemctl status prometheus
```

# Grafana


![image](https://github.com/user-attachments/assets/d308e9d4-5d75-455e-9e1b-33e359979ff3)

**Install Grafana on Ubuntu 22.04 and Set it up to Work with Prometheus**

**Step 1: Install Dependencies:**

First, ensure that all necessary dependencies are installed:

```
sudo apt-get update
sudo apt-get install -y apt-transport-https software-properties-common
```

**Step 2: Add the GPG Key:**

Add the GPG key for Grafana:

```
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
```

**Step 3: Add Grafana Repository:**

Add the repository for Grafana stable releases:

```
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
```

**Step 4: Update and Install Grafana:**

Update the package list and install Grafana:

```
sudo apt-get update
sudo apt-get -y install grafana
```

**Step 5: Enable and Start Grafana Service:**

To automatically start Grafana after a reboot, enable the service:

```
sudo systemctl enable grafana-server
```

Then, start Grafana:

```
sudo systemctl start grafana-server
```

**Step 6: Check Grafana Status:**

Verify the status of the Grafana service to ensure it's running correctly:

```
sudo systemctl status grafana-server
```

**Step 7: Access Grafana Web Interface:**

Open a web browser and navigate to Grafana using your server's IP address. The default port for Grafana is 3000. For example:

`http://<your-server-ip>:3000`

# **Kubernetes**
![image](https://github.com/user-attachments/assets/aaa7e04d-28b6-4559-b8b8-cba663234332)



**Create Kubernetes Cluster with Nodegroups**

In this phase, you'll set up a Kubernetes cluster with node groups. This will provide a scalable environment to deploy and manage your applications.

**Monitor Kubernetes with Prometheus**

Prometheus is a powerful monitoring and alerting toolkit, and you'll use it to monitor your Kubernetes cluster. Additionally, you'll install the node exporter using Helm to collect metrics from your cluster nodes.

**Install Node Exporter using Helm**

To begin monitoring your Kubernetes cluster, you'll install the Prometheus Node Exporter. This component allows you to collect system-level metrics from your cluster nodes. Here are the steps to install the Node Exporter using Helm:

1. Add the Prometheus Community Helm repository:
    
    ```
    helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
    ```
    
2. Create a Kubernetes namespace for the Node Exporter:
    
    ```
    kubectl create namespace prometheus-node-exporter
    ```
    
3. Install the Node Exporter using Helm:
    
    ```
    helm install prometheus-node-exporter prometheus-community/prometheus-node-exporter --namespace prometheus-node-exporter
    ```
    

Add a Job to Scrape Metrics on nodeip:9001/metrics in prometheus.yml:

Update your Prometheus configuration (prometheus.yml) to add a new job for scraping metrics from nodeip:9001/metrics. You can do this by adding the following configuration to your prometheus.yml file:

```
  - job_name: 'Netflix'
    metrics_path: '/metrics'
    static_configs:
      - targets: ['node1Ip:9100']

```

Replace 'your-job-name' with a descriptive name for your job. The static_configs section specifies the targets to scrape metrics from, and in this case, it's set to nodeip:9001.

### **Install Ansible (If Not Installed)**


![image](https://github.com/user-attachments/assets/78a497ea-564e-4f7a-8871-87f1609b6862)

```bash

sudo apt update

sudo apt update && sudo apt install ansible -y

```

### **Check Version**

```bash
b
ansible --version

```

# DataDog


![image](https://github.com/user-attachments/assets/5e6f3868-ecb7-47c7-a935-2a78b0fbe443)

To install Datadog on a Linux Ubuntu system, use the following command:

```bash

DD_API_KEY=<your_datadog_api_key> sudo -E bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script.sh)"

```

### Steps:

1. Replace `<your_datadog_api_key>` with your actual Datadog API key. You can find this in your Datadog account under **Integrations > APIs**.
2. This command:
    - Downloads the Datadog installation script.
    - Executes the script to install the Datadog Agent on your system.

After installation, verify that the Datadog agent is running with:














