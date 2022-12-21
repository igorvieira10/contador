<h1 align="center">Contador de obstáculos</h1>
 
**Descrição**: Pacote criado para realizar a contagem de obstáculos em um ambiente.
 
## Visão geral
 
Reconhecer e interagir com o ambiente é de total importância no âmbito da robótica móvel, visto que uma modelagem mais precisa do mundo permite ao robô ter mais autonomia, tomando decisões mais otimizadas para lidar com possíveis complicações em sua rotina, assim como obstáculos dinâmicos. Técnicas de visão computacional vem sendo a maneira implementada para realizar a contagem de objetos e estimar a posição do mesmo no mundo. Este pacote utiliza o sensor LiDAR para realizar a localização e contagem de objetos no mundo através da clusterização dos pontos lidos.
 
---
 
## 1. Requisitos
 
1. Ros Humble
  - Nav2
  - Gazebo
2. Ubuntu 2022
 
---
 
## 2. Instalação
 
Copie o repositório do Github para o workspace do ros:
 
```bash
$ cd ros_ws2/src
$ git clone https://github.com/igorvieira10/myread
$ rosdep install -i --from-path src --rosdistro humble -y
```
A seguir, será necessário realizar o *build* do pacote no *workspace* desejado.
 
```bash
$ source /opt/ros/humble/setup.bash
$ cd ros_ws2
$ colcon build
$ . install/local_setup.bash
```
---
## 3. Execução
 
O launch utilizado irá executar o ambiente de simulação Gazebo, o ambiente de visualização Rviz e o código responsável pela movimentação e contatem de objetos. Este é executado através do comando:
 
```bash
ros2 launch nav2_bringup trial2.py headless:=False```

---
 
## 4. Resultados
 

 
 
---
 
## 5. Algorítmo
 
---
 
## 6. Aprimoramentos
 
Tendo em vista que a navegação foi realizada a partir de um controlador de robô uniciclo, esta pode ser alterada para pelo stack de navegação Nav2, tornando o sistema mais robusto e confiável, além de ter mais suporte pela comunidade e possibilitar utilizar diferentes tipos de controladores para verificar a performance do algoritmo.
 
 
 
---
 
## 7. Possíveis Aplicações

Existem várias aplicações para detecção e contagem de objetos. Muitas aplicações envolvem questões de exploração, como a identificação e exploração do ambiente; manutenção, conhecendo o ambiente previamente é possível verificar a integridade de estruturas físicas como pilares, colunas ou canos; ou até aplicações na indústria, como, por exemplo, na indústria madeireira, onde teria a aplicação manter contabilizado as árvores plantadas.
