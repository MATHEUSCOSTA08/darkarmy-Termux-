# darkarmy-Termux-
       Instalação Termux aberto  pkg install git  pkg install python  git clone https://github.com/D4RK-4RMY/DARKARMY.git  cd DARKARMY  chmod +x darkarmy.py  python2 darkarmy.py 

D4RK-4RMY
/
DARKARMY
Público
Código
Problemas
Requisições pull
Ações
Projetos
Segurança
Conhecimentos
DARKARMY/install.sh _
@1ucif3r
1ucif3r pequena correção
 1 colaborador
106 linhas (88 sloc)  3,58 KB
#! /bin/bash

definir -e

Claro

PRETO= ' \e[30m '
VERMELHO= ' \e[31m '
VERDE= ' \e[92m '
AMARELO= ' \e[33m '
LARANJA= ' \e[93m '
AZUL= ' \e[34m '
ROXO= ' \e[35m '
CIANO= ' \e[96m '
BRANCO= ' \e[37m '
NC= ' \e[0m '
purpal= ' \033[35m '


Claro

contador=0
(

enquanto  :
Faz
gato << EOF
XXX
$contador
Carregando DARKARMY INSTALLER ....( $counter %):
XXX
EOF

(( contador += 20  ))
[ $counter  -eq 100 ] &&  break

dormir 1
feito
) |
whiptail --title " DARKARMY " --gauge " Aguarde " 7 70 0



Claro

echo -e " ${RED}  "
eco  " "                                                                         
echo  "   ██████ █████ ██████ ██ ██ █████ ██████ ███ ███ ██ ██         " ;
echo  "   ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ████ ████ ██ ██          " ; 
echo  "   ██ ██ ███████ ██████ █████ ███████ ██████ ██ ████ ██ ████           " ;
echo  "   ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██            " ;
echo  "   ██████ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ ██ V2.1      " ;
eco  "                                                                              " ;
echo  " Bem-                                      vindo ao instalador DARKARMY            " ;
echo -e " ${GREEN} ========================================== ========================= ${NC}  "                                                                                                                                                                                                                                
echo -e " ${BLUE}    www.dark4rmy.in | Instagram.com/0x1ucif3r | Github.com/D4RK-4RMY ${NC} "
echo -e " ${GREEN} ========================================== ========================= ${NC}           "
echo -e " ${RED}                                    [!] Esta ferramenta deve ser executada como ROOT [!] ${NC} \n "
eco  " "
echo -e " ${CYAN} [>] Pressione ENTER para instalar o DARKARMY, CTRL+C para abortar. ${NC} "
ler ENTRADA
eco  " "

if [ " $PREFIX "  =  " /data/data/com.termux/files/usr " ] ;  então
    INSTALL_DIR= " $PREFIX /usr/share/doc/DARKARMY "
    BIN_DIR= " $PREFIX /usr/bin/ "
    pkg install -y git python2
outro
    INSTALL_DIR= " /usr/share/doc/DARKARMY "
    BIN_DIR= " /usr/bin/ "
fi

echo  " [✔] Verificando diretórios... " ;
se [ -d  " $INSTALL_DIR " ] ;  então
    echo  " [!] Um diretório DARKARMY foi encontrado.. Deseja substituí-lo? [s/n]: "  ;
    leia mamãe
    if [ " $mama "  =  " y " ] ;  então
        rm -R " $INSTALL_DIR "
    outro
        saída
    fi
fi

echo  " [✔] Instalando... " ;
eco  " " ;
git clone https://github.com/D4RK-4RMY/DARKARMY.git " $INSTALL_DIR " ;
echo  " #!/bin/bash
python2 $INSTALL_DIR /darkarmy.py "  ' ${1+"$@"} '  > DARKARMY ;
chmod +x DARKARMY ;
sudo cp DARKARMY /usr/bin/ ;
rm DARKARMY ;


se [ -d  " $INSTALL_DIR " ] ;
então
    eco  " " ;
        echo  " [✔] Instalado com sucesso!!!\n\n " ;
        echo -e $GREEN  "        [+]++++++++++++++++++++++++++++++++++++++++++++++ ++++++++++++++++++++++[+] "
        eco             "        [+] [+] "
        echo -e $GREEN  "        [+] ✔✔✔ Agora é só digitar Terminal (DARKARMY) ✔✔✔ [+] "
        eco             "        [+] [+] "
        echo -e $GREEN  "        [+]++++++++++++++++++++++++++++++++++++++++++++++ ++++++++++++++++++++++[+] "
outro
    echo  " [✘] Falha na instalação Faça corretamente novamente NIGGA !!! [✘] " ;
    saída
