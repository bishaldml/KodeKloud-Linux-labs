# Custom Apache User Setup
#### Task's:
1. Create a user named anita on App server 3 within the Stratos Datacenter.
2. Assign a unique UID 1449 and designate the home directory as /var/www/anita.
#### Solutions:
Step-1: sudo useradd -u 1449 -d /var/www/anita anita

Step-2: vi script.sh
```
sudo useradd -u 1449 -d /var/www/anita anita
sudo mkdir -p /var/www/anita
sudo chown anita:anita /var/www/anita
sudo passwd anita
```

Step-3: sh script.sh

Step-4: cat /etc/passwd | grep anita
