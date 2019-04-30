# Deployment instructions for Group 18 Augur Project

### Instructions for getting the app running on an EC2 instance

1. SSH into your EC2 instance
2. Clone augur
3. Create a python virtual environment with 'venv augur'
4. activate the virtual environment with 'source augur/bin/activate'
5. run 'make install-dev'
6. run 'nohup make dev-start &'
 - This command keeps the app running even when you logout, make sure you hit enter twice!
7. run 'cat logs/backend.log' and 'cat logs/frontend.log' to make sure there were no errors.
