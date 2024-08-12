# Deployment steps
1. Run Jenkins server as docker container:
    
```
    sudo docker run -itd --name jenkins   -p 8080:8080 -p 50000:50000   -v ./:/var/jenkins_home   jenkins/jenkins:lts
    sudo docker ps

```

2. Install terrafform in Jenkins server:

```
    sudo docker exec -it --user=root jenkins bash
    apt update
    apt install wget
    wget https://releases.hashicorp.com/terraform/1.6.0/terraform_1.6.0_linux_amd64.zip
    unzip terraform_1.6.0_linux_amd64.zip
    sudo mv terraform /usr/local/bin/
    mv terraform /usr/local/bin/
    terraform version

```

3. Configure aws cli 

```
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    unzip awscliv2.zip
    sudo ./aws/install
    ./aws/install

```

4. AWS configure

```
    aws configure

```

5. test aws cli

```
    aws s3 ls

```
