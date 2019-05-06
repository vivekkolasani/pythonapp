## Changes made:-

1) port number 5001 exposed in dockerfile, but the same is not updated in app.py 
   Made the necessary changes i.e., initialized port no 5001 in app.py
   app.run(host='0.0.0.0', port=int("5001"))

2) In the "docker-compose.yml", the flask app is listening on port no 80 according to flaskapp.conf. But the port number was not in      order in the yml file. Changed the ports accordingly.
    "8080:80"
    
3) In the yml file, local folder where the data need to be stored is specified incorrectly.
   "data" -> "./data"
   
4) Included "restart:always" just to makee sure the system wont shutdown if the postgresql doesnt start.
