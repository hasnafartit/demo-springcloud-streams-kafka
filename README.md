# demo-springcloud-streams-kafka

Kafka offre un cluster de brokers qui permet d'echanger les messages entre les applications 

Pour demarer kafka il faut tout d'abord demarer zookeeper qui fait la coordination entre les instance de kafka et puis demarer le serveur kafka 

![image](https://user-images.githubusercontent.com/84719124/172861167-b96830c8-4ce5-449e-9876-b739f3e3eee3.png)


puis on a lancer un producer(permet de publier un flux d'enregistrements vers des topics kafka)  et  un customer(permet de s'abonné a un ou plusieurs topcs kafka et de traiter le flux d'enregistrements qui lui sont transmis) pour tester le serveur kafka

![image](https://user-images.githubusercontent.com/84719124/172861410-04031fa1-a430-4efc-b3c6-4843f4aed009.png)

le teste :

![image](https://user-images.githubusercontent.com/84719124/172861469-4f4343f6-8d07-43d5-b585-e82acfe0b472.png)


Apres on a creer une application spring boot:

   Dans la premiere partie on a lancer kafka console consumer puis on a lancer l'app rest controller qu'on a creé
      
  ![image](https://user-images.githubusercontent.com/84719124/172869819-f75f1331-f8f0-43dc-b7cf-729f4e87b606.png)

  
 puis on a lancer le navigateur(un browser) puis on a envoyer une requete http avec get (publish avec les parametre) le rest controller va recuperer les parametres et apres il a publié le message(pageEvent) sur le topic 
 
 ![image](https://user-images.githubusercontent.com/84719124/172869910-425d023b-25eb-4457-b3c1-803419480d1a.png)


![image](https://user-images.githubusercontent.com/84719124/172869946-70ee8ce2-52ce-4d9a-afc8-e572aabdaf83.png)


  Dans la 2eme partie on a creer un consumer (avec Consumer)  qui lire les messages envoyé par un topic et les afficher 
 
 (ici on a le tester avec le message envoyer par la requete http)
 
  ![image](https://user-images.githubusercontent.com/84719124/172872168-3259e933-fad2-423c-8dbb-46af0f4a3ee5.png)


(ici on a le tester avec le message envoyer par un producer sur cmd)

![image](https://user-images.githubusercontent.com/84719124/172873319-1a864616-c103-4193-88ec-6bfca163a0c8.png)


Dans la 3eme partie on a creé un producer en utilisant la fonction Supplier qui permet de publier dans un topic 

(ici on a lire les messages par un consumer sur cmd)

![image](https://user-images.githubusercontent.com/84719124/172874247-cc5f8929-db8a-4258-9e46-d4d3c87e9c6d.png)



Dans la 4eme partie on a creé une application où on a un consumer et un producer en meme temps,notre application prendre en input un enregistrement envoyé par un topic et puis il va faire un traitement et renvoie un enregistrement qu'elle le publier dans un autre topic


![image](https://user-images.githubusercontent.com/84719124/172877190-a62a10cf-86a0-46a2-936d-37a803556243.png)


(predre les enregistrement envoyer par une requete http en input)

![image](https://user-images.githubusercontent.com/84719124/172877243-3c0a0ea3-ccd6-44c1-b1f3-4eb57c94e345.png)

![image](https://user-images.githubusercontent.com/84719124/172877288-4ad2bd1d-6be3-44ec-9912-5f3014a9e5a1.png)


(predre les enregistrement publier par le producer qu'on a creer par supplier en input)

![image](https://user-images.githubusercontent.com/84719124/172877631-eec6c6cb-928f-4a70-adb9-fa0a055126f5.png)


Dans la 5eme partie on a utiliser kstream qui permet de lire un enregistrement envoyé par un topic puis il faire des calcules en temps réel et renvoie le resultat au bout d'une période precise dans un autre topic 
  
  ![image](https://user-images.githubusercontent.com/84719124/172881392-ecfeb8a1-f41b-4460-b460-154a341d3f6e.png)

teste 

![image](https://user-images.githubusercontent.com/84719124/172881424-7e6acecf-7881-459d-a3e9-3267ce54215b.png)


un autre exemple :

![image](https://user-images.githubusercontent.com/84719124/172882203-ec17c634-66d5-4b1c-aa90-b868c3d3332f.png)

![image](https://user-images.githubusercontent.com/84719124/172882300-903b0f2e-40fe-453d-b6da-8cbf01569e92.png)



Apres on a creer une methode de type Flux (dans le controleur) qui permet d'afficher le resultat de kstream en temps reel dans le navigateur 

![image](https://user-images.githubusercontent.com/84719124/172884166-e33bc68b-a961-43c6-aec2-52faea25dac3.png)


resultat :

![image](https://user-images.githubusercontent.com/84719124/172884243-633e8ae0-747a-42df-a99b-4a50d47bde1f.png)

puis on a creer page html qui permet d'afficher le graphe en temps reel 

![image](https://user-images.githubusercontent.com/84719124/172884661-f5198529-869b-4df8-b050-3a62943c5ae2.png)


  

  
  
