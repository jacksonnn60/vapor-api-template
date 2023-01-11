# SETUP digital ocean server

links:
- digital ocean setup: https://docs.vapor.codes/deploy/digital-ocean/

1.Create new droplet on 'Digital Ocean'

2.Download Swift
- from swift.org, (version X86_64)
- extract swift tar using tar xzf swift.tar

3. Add export swift to ~/.bashrc
- vim ~/.bashrc
- export PATH=~/pathto swift bin:"${PATH}"
- run: swift --version

4. Install Dependencies for Swift & Vapor
- run: sudo apt-get update
- run: sudo apt-get install clang libicu-dev libatomic1 build-essential pkg-config
- run: sudo apt-get install openssl libssl-dev zlib1g-dev libsqlite3-dev

5. Install Vapor and Docker
- docker: https://docs.docker.com/engine/install/ubuntu/
- vapor: https://docs.vapor.codes/install/linux/

6. Configure file wal
- ufw allow OpenSSH
- ufw enable

7. Allow HTTP: sudo ufw allow http

8. Compose db for server: docker compose up db
