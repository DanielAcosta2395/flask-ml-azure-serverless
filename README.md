python3 -m venv ~/.flask-ml-azure

source ~/.flask-ml-azure/bin/activate

make install

az webapp up -n <your-appservice>