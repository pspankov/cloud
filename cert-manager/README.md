# Cert-manager

1. Create private key for the certificate authority

```
openssl genrsa -out ca.key 4096
```

2. Generate CA certficate from the key

```
openssl req -new -x509 -sha256 -days 10950 -key ca.key -out ca.crt
```

3. Create secret yaml file from the key and certificate in base64 format

```
kubectl create secret tls nginx-ca-secret -n cert-manager --cert=ca.crt --key=ca.key --dry-run=client  --output=yaml > nginx-ca-secret.yaml
```

4. Apply the two manifest files the we created

```
kubectl apply -f nginx-ca-secret.yaml
kubectl apply -f nginx-clusterissuer.yaml
```
