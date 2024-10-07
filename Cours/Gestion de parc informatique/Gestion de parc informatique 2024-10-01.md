Network Editor
-supprimer toutes les cartes réseaux VMnet
-créer un nouveau réseau VM Net 0
-affecter à VMNet 0 -> NAT
-vérifier connexion et DHCP -> coché
-adresse du réseau NAT -> 10.10.10.0
-appliquer

Setting des VM : Choisir Custom VMNet 0 (NAT)

Changement adresse ip dynamique en statique:

/etc/network/interfaces

iface ens33 inet static
	address 10.10.10.100
	netmask 255.255.255.0
	gateway 10.10.10.2
	dns-nameservers 8.8.8.8 4.4.4.4

/etc/resolv.conf

	nameserver 10.10.10.2
