## As boas práticas do Ansible (via Medium post)


1. Primeiro ponto aqui, quando você efetuar a instalação do Ansible via `yum` ou `apt` (gerenciador de pacotes de sistemas LINUX), será criado um caminho absoluto dentro do diretorio `/etc` do seu sistema em `/etc/ansible`. Junto com a instalação ele mantém também o arquivo de configuração do Ansible ansible.cfg e o arquivo de inventário nomeado de hosts dentro desse diretório /etc/ansible Visando as boas práticas não executamos o Ansible nesse diretório, justamente por ser um diretório de configuração do sistema e por questões de segurança é melhor trabalhar fora desse diretório com o Ansible. O Ansible funciona bem de qualquer diretório do sistema, eu costumo usar o gerenciador de pacotes do Python nomeado de pip , ele mesmo se encarrega de instalar o Ansible e por padrão ele não cria esse diretório no /etc Nesse caso você deve criar a estrutura do Ansible em outro diretório, como exemplo, no /home de algum usuário que você esteja mais seguro de executar o Ansible.
