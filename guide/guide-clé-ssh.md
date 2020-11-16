La clé SSH permet de créer une connection entre l'ordi et un serveur. Il permet ainsi de modifier des documents situé dans un dossier sur le web. 
La synchronisation n'est instantannée. Il faut l'a générer. 
Passons à la création de la clés. 
- Ouvrir le terminal et écrire la commande ***ssh-keygen -t rsa***
- Des questions apparaissent, il ne faut pas répondre et taper sur ***entré***
- la clé apparaît sous cette forme ![clé ssh](https://www.hostinger.fr/tutoriels/wp-content/uploads/sites/9/2017/04/ssh-cle.png)
- Entrer la commande suivante ***cat .ssh/id_rsa.pub*** elle génère l'apparition de la clé ssh en format comme ci dessous
***ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDsFPPAZDvfJTekprwNcQ9jYHLGU0TPii9y2AXWJNkzBrCbowyPq4JWiVfScnSiEnHp1XW4Lr114q2KoAqzOygeNyXoQ7GZs07FitdlUZ7CZiaAHF7oP6PD947K0b5TTGJqGpWL5OsvLrgmuID6jueE594U3NUD78fGSKQmXXV6Wqi/fKqS8wWkiCFI0mxa6AUedPIDB4vPcRU6mPxvMcGe8bLQJYfSV2xukbVPwvNbBYg+voL2hv5DJxPzG+bSI0E1GdkryvNYIN2Ag8WXaCWJDAlfuGp18pyq2YrK8jjoYQI6PieWgmqvgfSO4GZq3HHUy3JR5nBsiVmN/yiQw11h80Kz42QJRacaHUC2UtNDrwSQTubKZUjI4NfOVwWLGX4wf7FVCn4VxM/F3CYhNkgt1k3cK7OR4ABMC3bpuNk4UpWu0AtU8Da4DSfD1L97aNbxLRHMZyWLbLEsny7lCEMelRbcLEfsw1gjW+SVOE4PrSqYCbXWc4VVYAQ/Yv0k/7s= dirdir@Diren***
- copier la ligne de formule et quitter le terminal, se rendre sur github, aller dans les paramètres (setting) en haut full à droite, 
puis dans les paramètre aller dans ***ssh and gpg keys***
- créer une nouvelle clé, la nommer, coller la ligne de code et enregistrer

logiquement à cette étape les clés permettent la syncronisation. Il faut dans un second temps installer git dans le pc
Chose que je n'arrive pas encore à faire car j'ai des messages d'erreur. 





