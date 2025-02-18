**Commutation :** transfert de connexions d'un ensemble de conducteur à un autre.

**1. Commutation de circuit :**

Le circuit est établi au préalable,  la ligne de communication entre l'émetteur et le récepteur est **réservée**. Si personne ne répond, un signal de retour annule la réservation de la ligne.
Une fois la communication établie, toutes les données empruntent ensuite ce même chemin prédéfini (signal numérique transmis entre commutateurs).

Mais la commutation de circuit coûte cher, surtout lorsque l'émetteur et le récepteur sont éloignés.

On a ici une **réservation de ressources dite déterministe.**

En 1971, **Louis Pouzin**, polytechnicien et chercheur de grand talent, propose quelque chose de totalement nouveau : un réseau maillé d'ordinateurs basé sur la commutation de paquets.

![Commutation de circuits](./img/commutationcircuits.png)

**2. Commutation de paquets (mieux que commutation de circuits):**

Dans ce type de commutation, aucun circuit n'est prédéfini entre l'émetteur et le récepteur.

Les paquets n'empruntent pas forcément le même chemin. C'est ce qu'on appelle **best effort delivery**.

La **réservation de ressources est dite indéterministe.**

La commutation par paquets est mieux que celle vue précédemment, parce que le fait de ne pas avoir à établir un circuit de bout en bout apporte une souplesse cruciale :

- Les données peuvent être découpées en morceaux
- Les noeuds peuvent organiser des fils d'attente
- Ce principe permet de partager les flux

Les moyens mis en oeuvre pour accélérer un lien sont :

- augmenter la cadence d'émission des bits (Mbits/s, Gb/s, ...)
- émettre les données en parallèle, en utilisant des techniques de multiplexage.

![Commutation de paquets](./img/commutationpaquets.png)

- Le réseau à commutation de paquets nécessite des nœuds d’aiguillage qui
sont, dans un premier temps, des ordinateurs (TCProgram), puis deviennent
des routeurs (TCProtocol) spécialisés (ou des Systèmes-Intermédiaires - OSI)
- Chaque paquet est entièrement chargé en mémoire avant d’être retransmis
- Comme aucune ressource n’est réservée au préalable, certains paquets
peuvent être rejetés en cas de congestion ou de destination inaccessible.

IP (Internet Protocol) ne transporte rien, il organise le système postal. Sa force est liée à son mode déconnecté (c'est-à-dire qu'il n'établit pas de liaison continue entre l'expéditeur et le destinataire avant d'envoyer les données) et son indéterminisme (IP ne garantit pas un chemin unique ou prédéterminé pour les paquets).