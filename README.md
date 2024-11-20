# Medical_Chatbot

![Gemini_Generated_Image_7pxdtv7pxdtv7pxd](https://github.com/user-attachments/assets/65b45397-957a-402b-b572-b8f0ac3d8a5c)

The "medical chatbot" project aims to develop an advanced AI-powered conversational system tailored for the healthcare sector. This innovative solution leverages the capabilities of Large Language Models (LLMs) in conjunction with Pinecone and LangChain technologies. The primary objectives of this chatbot include:

    Providing precise answers to health-related inquiries
    Offering medical guidance
    Efficiently retrieving pertinent medical information

Key features and components of the project include:

    Integration with Pinecone's vector database for scalable and efficient data retrieval
    Implementation of a retrieval-augmented generation (RAG) pipeline
    Design and configuration of sophisticated conversational flows
    Strict adherence to health information privacy standards
    Rigorous validation processes to ensure medical accuracy of outputs

This versatile chatbot solution is particularly well-suited for applications such as:

    Intelligent virtual assistants for patient support
    Telemedicine platforms
    Healthcare research tools

By combining cutting-edge AI technologies with domain-specific knowledge, this medical chatbot project aims to revolutionize the way healthcare information is accessed and utilized in various medical contexts.




# How to run?
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


```bash
# run the following command to store embeddings to pinecone
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```


### Techstack Used:

- Python
- LangChain
- Flask
- GPT
- Pinecone


# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 970547337635.dkr.ecr.ap-south-1.amazonaws.com/medicalchatbot

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO
   - PINECONE_API_KEY
   - OPENAI_API_KEY

    
