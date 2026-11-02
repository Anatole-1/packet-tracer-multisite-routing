# Configurations – Projet réseaux avancés

Configuration complète de chaque équipement, exportée depuis le fichier Packet Tracer.
Les mots de passe et numéros de série sont masqués ; les interfaces sans configuration sont omises.
Les fichiers bruts (un par équipement) sont dans [`configs/`](configs/).

## Sommaire

- [Router3](#router3) – Router Router-PT
- [Router4](#router4) – Router Router-PT
- [Router5](#router5) – Router Router-PT
- [Router6](#router6) – Router Router-PT
- [Router7](#router7) – Router Router-PT
- [Router8](#router8) – Router Router-PT
- [Router9](#router9) – Router Router-PT
- [Router10](#router10) – Router Router-PT
- [Router11](#router11) – Router Router-PT
- [Router12](#router12) – Router Router-PT
- [Switch0](#switch0) – Switch 2960-24TT
- [Switch3](#switch3) – Switch 2960-24TT
- [Switch4](#switch4) – Switch 2960-24TT
- [Switch5](#switch5) – Switch 2960-24TT
- [Switch6](#switch6) – Switch 2960-24TT
- [Switch7](#switch7) – Switch 2960-24TT
- [Switch8](#switch8) – Switch 2960-24TT
- [Switch9](#switch9) – Switch 2960-24TT
- [Switch10](#switch10) – Switch 2960-24TT
- [Switch11](#switch11) – Switch 2960-24TT
- [Postes et serveurs](#postes-et-serveurs)

## Postes et serveurs

| Nom | Type | Adresse IP | Masque | Passerelle | DNS |
|---|---|---|---|---|---|
| 2.1 | Pc | 172.19.0.10 | 255.255.255.248 | 172.19.0.9 | – |
| 2.2 | Pc | 172.19.0.11 | 255.255.255.248 | 172.19.0.9 | – |
| 2.3 | Pc | 172.19.0.4 | 255.255.255.248 | 172.19.0.1 | – |
| 2.4 | Pc | 172.19.0.18 | 255.255.255.248 | 172.19.0.17 | – |
| 2.5 | Pc | 172.19.0.19 | 255.255.255.248 | 172.19.0.17 | – |
| PC0 | Pc | 14.0.0.4 | 255.255.255.248 | 14.0.0.1 | – |
| PC1.1 | Pc | 197.45.12.2 | 255.255.255.248 | 197.45.12.1 | – |
| PC1.2 | Pc | 197.45.12.3 | 255.255.255.248 | 197.45.12.1 | – |
| PC1.3 | Pc | 197.45.12.20 | 255.255.255.248 | 197.45.12.17 | – |
| PC1.4 | Pc | 197.45.12.10 | 255.255.255.248 | 197.45.12.9 | – |
| PC1.5 | Pc | 197.45.12.11 | 255.255.255.248 | 197.45.12.9 | – |
| PC3.1 | Pc | 159.76.0.10 | 255.255.255.248 | 159.76.0.9 | – |
| PC3.2 | Pc | 159.76.0.11 | 255.255.255.248 | 159.76.0.9 | – |
| PC3.3 | Pc | 159.76.0.12 | 255.255.255.248 | 159.76.0.9 | – |
| PC3.4 | Pc | 159.76.0.13 | 255.255.255.248 | 159.76.0.9 | – |
| PC3.5 | Pc | 159.76.0.18 | 255.255.255.248 | 159.76.0.17 | – |
| PC3.6 | Pc | 159.76.0.19 | 255.255.255.248 | 159.76.0.17 | – |
| PC3.7 | Pc | 159.76.0.20 | 255.255.255.248 | 159.76.0.17 | – |
| PC3.8 | Pc | 159.76.0.21 | 255.255.255.248 | 159.76.0.17 | – |
| PC3.9 | Pc | 159.76.0.26 | 255.255.255.252 | 159.76.0.25 | – |

## Router3

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 197.45.12.9 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 197.45.12.19 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 197.45.12.17 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router4

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 197.45.12.1 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 197.45.12.18 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
!
interface Serial3/0
 no ip address
 clock rate 2000000
!
interface FastEthernet4/0
 no ip address
!
interface FastEthernet5/0
 no ip address
!
ip classless
ip route 0.0.0.0 0.0.0.0 197.45.12.17 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router5

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 14.0.0.1 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 197.45.12.17 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 197.45.12.0 255.255.255.248 197.45.12.18 
ip route 197.45.12.8 255.255.255.248 197.45.12.19 
ip route 172.19.0.0 255.255.0.0 14.0.0.2 
ip route 159.76.0.0 255.255.0.0 14.0.0.3 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router6

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 14.0.0.2 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 172.19.0.1 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 14.0.0.1 
ip route 172.19.0.8 255.255.255.248 172.19.0.2 
ip route 172.19.0.16 255.255.255.248 172.19.0.3 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router7

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 14.0.0.3 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 159.76.0.1 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 14.0.0.1 
ip route 159.76.0.8 255.255.255.248 159.76.0.2 
ip route 159.76.0.16 255.255.255.248 159.76.0.4 
ip route 159.76.0.24 255.255.255.248 159.76.0.3 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router8

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 172.19.0.9 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 172.19.0.2 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 172.19.0.1 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router9

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 172.19.0.17 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 172.19.0.3 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 172.19.0.1 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router10

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 159.76.0.25 255.255.255.252
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 159.76.0.3 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 159.76.0.1 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router11

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 159.76.0.17 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 159.76.0.4 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 159.76.0.1 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Router12

Router · modèle Router-PT · hostname `Router`

```cisco
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
ip cef
no ipv6 cef
!
interface FastEthernet0/0
 ip address 159.76.0.9 255.255.255.248
 duplex auto
 speed auto
!
interface FastEthernet1/0
 ip address 159.76.0.2 255.255.255.248
 duplex auto
 speed auto
!
interface Serial2/0
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial3/0
 no ip address
 clock rate 2000000
 shutdown
!
interface FastEthernet4/0
 no ip address
 shutdown
!
interface FastEthernet5/0
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 159.76.0.1 
!
ip flow-export version 9
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
end
```

## Switch0

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch3

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch4

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch5

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch6

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch7

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch8

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch9

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch10

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```

## Switch11

Switch · modèle 2960-24TT · hostname `Switch`

```cisco
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Vlan1
 no ip address
 shutdown
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end
```
