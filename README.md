# Generate SSH public key
ssh-keygen -t rsa

# Clone the repo
git clone https://github.com/DanielAcosta2395/flask-ml-azure-serverless.git

# Create a virtual python environment
python3 -m venv ~/.flask-ml-azure

# Run the virtual environment
source ~/.flask-ml-azure/bin/activate

# Install dependencies
make install

# Create a webapp service in Azure account
az webapp up -n danisflaskmlazure

OR

az webapp up --name danisflaskmlazure --resource-group Azuredevops --sku B1 --logs --runtime "PYTHON:3.10"

# List webapps services running
az webapp list-runtimes

# To apply new changes
az webapp up