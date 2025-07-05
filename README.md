# i2internVoltDB1
# VoltDB Docker ile Çalıştırma 

Bu proje, i2i Systems staj programı kapsamında geliştirildi. Ödevin amacı, VoltDB veritabanını Docker konteyneri olarak çalıştırmak, temel SQL işlemleri yapmak ve bu uygulamayı bulut ortamına (GCP veya AWS) taşıma sürecini deneyimlemektir.

## Proje İçeriği

- VoltDB Community Edition Docker imajının kullanılması  
- Docker ağı (network) oluşturularak VoltDB konteynerinin başlatılması  
- VoltDB veritabanı içine SQL sorguları ile tablo oluşturulması, veri eklenmesi ve sorgulanması  
- Kurulum ve çalıştırma adımlarının hem yerel makinede hem de Google Cloud Platform (GCP) üzerinde uygulanması  
- Docker ve VoltDB komutlarının temel düzeyde kullanımı  
- GCP üzerinde Ubuntu 22.04 LTS VM kurulumu, Docker kurulumu ve VoltDB konteynerinin çalıştırılması

## Kullanılan Teknolojiler

- Docker  
- VoltDB Community Edition  
- Google Cloud Platform (GCP) veya AWS (opsiyonel)  
- Ubuntu 22.04 LTS (VM işletim sistemi)  

## Kurulum ve Çalıştırma Adımları

 
   ```bash
   Docker İmajının İndirilmesi  
   docker pull basvanbeek/voltdb-community:latest
   Docker Ağı Oluşturma:
   docker network create voltLocalCluster
   VoltDB Konteynerinin Başlatılması:
   docker run -d -P -e HOST_COUNT=1 -e HOSTS=node1 --name=node1 --network=voltLocalCluster   basvanbeek/voltdb-community:latest
   SQL Terminaline Bağlanma:
   docker exec -it node1 sqlcmd



   
