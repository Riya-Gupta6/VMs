# VMs
Create an Azure virtual machine
az vm create --resource-group "learn-76fc657d-2944-42f7-a91d-81bfb0b3c01b" --name my-vm --public-ip-sku Standard --image Ubuntu2204 --admin-username azureuser --generate-ssh-keys
az vm extension set --resource-group "learn-76fc657d-2944-42f7-a91d-81bfb0b3c01b" --vm-name my-vm --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
