1. login
2. source augur/bin/activate
3. cd augur
4. git pull
5. make install-dev
6. nohup make dev-start &  
  - keeps it running when you logout.
  - you have to hit return twice
7. cat logs/backend.log
  - make sure there are no errors
  - biggest error is not having updated augur.config.json
