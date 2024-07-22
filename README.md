# Mock data-tooling Minio

Minio servant de mock S3 pour le projet mock data-tooling

Afin d'avoir un certificat valide, les ingress doivent être un sous le domaine *.dev.numerique-interieur.com

## Secrets

Il faut créer un secret nommé secrets.yml.dec avec le contenu suivant:

```yaml
apiVersion: isindir.github.com/v1alpha3
kind: SopsSecret
metadata:
  name: secret-mock-data-tooling-minio
spec:
  secretTemplates:
    - name: minio-root
      stringData:
        root-user: admin
        root-password: MonSuperMotDePasse1234!
```

Voir fichier **conf/secrets/ovh/dev/secrets.yml.dec.exemple**