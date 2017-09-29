# conrepG7DL165

1) Login to server machine
2) wget https://raw.githubusercontent.com/dimsk/conrepG7DL165/master/conrepDL165G7-SL165zG7-SL165sG7_20111104.xml
3) wget https://raw.githubusercontent.com/dimsk/conrepG7DL165/master/dump.dmp
4) docker run --rm -it -v /:/media/host --privileged dimsik/conrep910 -l -fdump.dmp -xconrepDL165G7-SL165zG7-SL165sG7_20111104.xml
