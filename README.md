# Prerequisites:

  1) Place your AWS credentails under .aws/credentails

# Steps:

  1)Give the package execution permissionon.
  2)Execute the package using command ./neuron.

# Usage:

  # Examples:-

    curl -H "Content-Type: application/json" -X POST -d '{"InstanceName":"consul-machine","ImageId":"ami-6ff64712","SubnetId":"subnet-572eaa3e","KeyName":"ranjith_acc","Flavor":"t2.micro","UserData":"echo 'nothing'","AssignPubIp":true,"Cloud": {"Cloud":"aws","Region":"eu-west-3"}}' http://<your domain/ip>:8080/createserver

    curl -H "Content-Type: application/json" -X POST -d '{"AppVersion":"2.8","UniqueId":"2.8"}' http://<your domain/ip>:8080/startbuildmachine

    curl -H "Content-Type: application/json" -X GET -d '{"SubnetId":"subnet-d81893b1","Cloud": {"Cloud":"aws","Region":"ap-south-1"}}' http://<your domain/ip>:8080/getservers

    curl -H "Content-Type: application/json" -X POST -d '{"InstanceId":["i-070e496ff40c208af"],"Cloud": {"Cloud":"aws","Region":"eu-west-3"}}' http://<your domain/ip>:8080/deleteservers

    curl -H "Content-Type: application/json" -X POST -d '{"Name":"Test_Network","VpcCidr":"192.168.0.0/16","SubCidr":["192.168.10.0/24","192.168.20.0/24"],"Type":"public","Ports":["8080","22","80","443"],"Cloud": {"Cloud":"aws","Region":"eu-west-3"}}' http://<your domain/ip>:8080/createnetwork

    curl -H "Content-Type: application/json" -X GET -d '{"Cloud":"aws","Region":"eu-west-3"}' http://<your domain/ip>:8080/getregions

    curl -H "Content-Type: application/json" -X GET -d '{"Cloud":"aws","Region":"eu-west-3"}' http://<your domain/ip>:8080/getsubnets

    curl -H "Content-Type: application/json" -X GET -d '{"Cloud":"aws","Region":"eu-west-3"}' http://<your domain/ip>:8080/getallservers

  
# For UI:

  1) For UI of neuron, unzip the File neuronUI and host it on any webserver (preferably apache2).
  2) This UI has very minimal feature when compared to neron application alone.
  3) For the Neuron UI to work PHP should be installed in the machine where UI is hosted, and respective PHP modules of the webserver on which it is hosted.
  4) Once it is hosted one can access UI by hitting: http://<your domain/ip>/neuron/production/

# Coming Soon:

  1) Compactability with other clouds, Azure on priority.
  3) Few more endpoints for the operations.
  
For doubts and more info please write to us @: [denginecore <dengine.core@mindtree.com>]
