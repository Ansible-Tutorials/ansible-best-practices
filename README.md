## As boas práticas do Ansible (via Medium post)

Opa, voltando com TUDO pessoal! Hoje vamos de Ansible, trazendo um [post](https://amauryborgesouza.medium.com/as-boas-pr%C3%A1ticas-do-ansible-que-ningu%C3%A9m-te-conta-e-que-n%C3%A3o-existem-no-google-4fcc3126ad1) mais à nível técnico e que eu acredito que seja legal de escrever e conversar, até porque, atualmente o Ansible é um dos projetos que mais crescem no GitHub, a documentação é fantástica e eu também vejo o pessoal super engajado na comunidade fazendo a diferença com o Ansible no dia a dia. Eu tenho trabalhado com a ferramenta em ambientes de produção e posso arriscar alguns centavos 😅 . Fiquem a vontade para apontar qualquer boa prática que você usa no seu trabalho/projeto e pode discordar também.


### Guia de boas práticas
1. Primeiro ponto aqui, quando você efetuar a instalação do Ansible via `yum` ou `apt` (gerenciador de pacotes de sistemas LINUX), será criado um caminho absoluto dentro do diretorio `/etc` do seu sistema em `/etc/ansible`. Junto com a instalação ele mantém também o arquivo de configuração do Ansible ansible.cfg e o arquivo de inventário nomeado de hosts dentro desse diretório /etc/ansible Visando as boas práticas não executamos o Ansible nesse diretório, justamente por ser um diretório de configuração do sistema e por questões de segurança é melhor trabalhar fora desse diretório com o Ansible. O Ansible funciona bem de qualquer diretório do sistema, eu costumo usar o gerenciador de pacotes do Python nomeado de pip , ele mesmo se encarrega de instalar o Ansible e por padrão ele não cria esse diretório no /etc Nesse caso você deve criar a estrutura do Ansible em outro diretório, como exemplo, no /home de algum usuário que você esteja mais seguro de executar o Ansible.

2. 
