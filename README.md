```
cd ~ && \
curl -fsSL -o /tmp/technitium.zip https://github.com/AngelGonePro/technitium-dns-docker-compose/raw/refs/heads/main/technitium-dns.zip && \
python3 -c "import zipfile; open('/tmp/deploy-update.sh','wb').write(zipfile.ZipFile('/tmp/technitium.zip').read('technitium-dns/deploy-update.sh'))" && \
sh /tmp/deploy-update.sh https://github.com/AngelGonePro/technitium-dns-docker-compose/raw/refs/heads/main/technitium-dns.zip technitium-dns && \
cp /tmp/deploy-update.sh technitium-dns/ && chmod +x technitium-dns/*.sh technitium-dns/helper/helper && rm -f /tmp/technitium.zip /tmp/deploy-update.sh
```
