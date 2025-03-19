# Mini-Projet Terraform : Déploiement d'une Infrastructure Complète

## Description
Ce projet a pour objectif de déployer une infrastructure complète sur AWS en utilisant les bonnes pratiques de Terraform. L'infrastructure comprend :
- Une instance EC2 avec NGINX installé automatiquement.
- Un volume EBS attaché à l'instance pour la persistance des données.
- Un Security Group pour gérer les règles de sécurité.
- Une IP publique attribuée à l'instance EC2.

Le projet est structuré en modules pour favoriser la réutilisation du code et simplifier la maintenance.

## Prérequis
- Un compte AWS.
- Terraform installé sur votre machine.
- Configuration des accès AWS avec des clés Access Key et Secret Key.

## Arborescence du Projet
```
.
├── main.tf
├── variables.tf
├── outputs.tf
├── modules
│   ├── ec2
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── ebs
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── security_group
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── public_ip
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
└── ip.txt
```

## Utilisation
1. **Initialisation du projet**
```bash
terraform init
```

2. **Validation du code**
```bash
terraform validate
terraform fmt
```

3. **Planification**
```bash
terraform plan
```

4. **Application du plan**
```bash
terraform apply
```

5. **Récupération de l'IP publique**
L'adresse IP publique sera automatiquement enregistrée dans le fichier `ip.txt`.

6. **Test de l'installation de NGINX**
Ouvrez un navigateur et accédez à l'IP publique via le port 80 :
```
http://<IP_PUBLIQUE>
```
Vous devriez voir la page par défaut de NGINX.

7. **Destruction de l'infrastructure**
Lorsque vous avez terminé vos tests, vous pouvez détruire l'infrastructure pour éviter les coûts :
```bash
terraform destroy
```

# Terraform<img width="1048" alt="Capture d’écran 2024-10-11 à 14 34 06" src="https://github.com/user-attachments/assets/1fe8b44d-7548-4922-bbf6-405b9862c848">
<img width="1166" alt="Capture d’écran 2024-10-11 à 14 33 32" src="https://github.com/user-attachments/assets/66a99ad2-c43e-4a40-bd30-c522d89c2157">
