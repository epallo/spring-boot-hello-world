#!/usr/bin/python
import SimpleHTTPServer
import SocketServer
import os
import socket
import json
import signal



f_exists = (os.path.exists("/home/enricopalomeno/python/appPID")) #for file

if f_exists == True:
	f = open("appPID", "r")
	text = f.read()
	print text
	f.close()
	var1=int(text)
	os.kill(var1, signal.SIGKILL)
	os.remove("/home/enricopalomeno/python/appPID")

'''
#get pid of current process
pid1=str(os.getpid())
file = open("appPID","w")
file.write(pid1)
file.close()

# create info.json
os.chdir(os.path.dirname(os.path.realpath(__file__)) + "/public")
info = {
	"host_name": socket.gethostname(),
	"version": 1
}
with open('info.json', 'w') as outfile:
    json.dump(info, outfile)


# configure and run the server
PORT = 9000
Handler = SimpleHTTPServer.SimpleHTTPRequestHandler
httpd = SocketServer.TCPServer(("", PORT), Handler)
print socket.gethostname()
httpd.serve_forever()
'''
