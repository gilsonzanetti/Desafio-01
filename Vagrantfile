Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.provider "virtualbox" do |vb|
    vb.name = "desafio-04"
        end

    config.vm.provision "shell" , inline: <<-SHELL
    sudo apt -y remove docker docker-engine docker.io containerd runc
    sudo apt update
    sudo apt -y install ca-certificates curl gnupg lsb-release
    sudo mkdir -p /etc/apt/keyrings
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    sudo apt update
    sudo apt -y install docker-ce docker-ce-cli containerd.io docker-compose-plugin
    sudo groupadd docker 
    sudo usermod -ag docker vagrant
    newgrp docker
    SHELL

end


     








           
    











    




