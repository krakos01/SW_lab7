# Sprawozdanie z zadania 7
### Polecenie użyte do zbudowania obrazu
```
docker buildx build -q -f Dockerfile --platform linux/arm64,linux/amd64 \
-t docker.io/krakos01/sw:zad7 --sbom=true --provenance=mode=max --push .
```

### Wynik polecenia do sprawdzenia podatności
Obraz nie ma podatności "Critical" ani "High". Jedyna podatność "Medium" jest zależna od obrazu alpine, ale na chwilę obecną nie ma nowszej.
```
docker scout cves docker.io/krakos01/sw:zad7 --platform linux/amd64
```
![obraz](https://github.com/user-attachments/assets/fcc970ab-0c67-4e5b-80e9-6380ed9dca65)

