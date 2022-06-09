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

  
 puis on a lancer le navigateur(un browser) puis on a envoyer une requete http avec get (publish avec les parametre) le rest controller va recuperer les parametres et apres il a publier le msg(pageEvent) sur le topic 
 
 ![image](https://user-images.githubusercontent.com/84719124/172869910-425d023b-25eb-4457-b3c1-803419480d1a.png)


![image](https://user-images.githubusercontent.com/84719124/172869946-70ee8ce2-52ce-4d9a-afc8-e572aabdaf83.png)




  
  
