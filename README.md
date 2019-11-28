# My Docker dev environment
PHP 7.3, MySQL 8.x, Apache2

# Usage
1. Copy/move .env.dist to .env
2. Change what you need in .env (set USER_ID to your UID)
3. run `docker-compose up -d`
4. run `docker exec -it dev-apache bash` -> `su developer`
