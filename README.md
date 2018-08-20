# ambiente-laravel-homestead
Configurações para iniciar um ambiente para desenvolvimento Laravel


1 - Instalar o vagrant:
https://www.vagrantup.com/

2 - Instalar o VirtualBox:
https://www.virtualbox.org/

3 - Instalar o homestead:
https://laravel.com/docs/5.6/homestead#first-steps

4 - Configurações Homestead.yaml

ip: "192.168.10.74"
memory: 2048
cpus: 1
provider: virtualbox

authorize: ~/.ssh/id_rsa.pub

keys:
    - ~/.ssh/id_rsa

folders:
    - map: ~/code
      to: /home/vagrant/code
    
    - map: CAMINHO PROJETO
      to: CAMINHO PROJETO NO VAGRANT /home/vagrant/...

sites:
    - map: homestead.test
      to: /home/vagrant/code/public

    - map: laravel.test
      to: CAMINHO PROJETO NO VAGRANT

databases:
    - homestead
    - NOME BANCO
name: homestead
hostname: homestead

# ports:
#     - send: 50000
#       to: 5000
#     - send: 7777
#       to: 777
#       protocol: udp

# blackfire:
#     - id: foo
#       token: bar
#       client-id: foo
#       client-token: bar

# zray:
#  If you've already freely registered Z-Ray, you can place the token here.
#     - email: foo@bar.com
#       token: foo
#  Don't forget to ensure that you have 'zray: "true"' for your site.

5 - Instalar plugin que autualiza o arquivo de Hosts automáticamente:
https://github.com/cogitatio/vagrant-hostsupdater
