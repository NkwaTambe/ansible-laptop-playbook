Vagrant.configure("2") do |config|

 
  config.vm.define "ansible-test" do |test|
    test.vm.hostname = "test"


    test.vm.box = "generic/ubuntu2004"

 
    test.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y ansible
    SHELL

    # Provision the VM using Ansible playbook
    test.vm.provision "ansible" do |ansible|
      ansible.playbook = "gis/laptop/playbooks/playbook.yml"
      ansible.compatibility_mode = "2.0"
      
      
          
      ansible.extra_vars = {
       setup_cargo: false,
       setup_sdkman: true,
       setup_nvm: false,
       setup_docker: true
        }
    end
  end
end

