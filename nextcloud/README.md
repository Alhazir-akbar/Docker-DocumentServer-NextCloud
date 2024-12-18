1. Pastikan Nextcloud dan OnlyOffice Berada dalam Jaringan Docker yang Sama
docker network create nextcloud_onlyoffice_network

# Restart Nextcloud
docker-compose -f /home/enigmap/aptika/produk-hukum-jdih/onlyOffice/docker/docker-compose-nextcloud.yaml down
docker-compose -f /home/enigmap/aptika/produk-hukum-jdih/onlyOffice/docker/docker-compose-nextcloud.yaml up -d

# Restart OnlyOffice
docker-compose -f /home/enigmap/Docker-DocumentServer/docker-compose.yml down
docker-compose -f /home/enigmap/Docker-DocumentServer/docker-compose.yml up -d
