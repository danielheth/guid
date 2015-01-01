# GUID
The only way to get a truely unique identifier is to have a central authority which issues that value after comparing it to all previously issued values.  guidd is that server and guid is the client that connects to get that unique value.

# Official Repository

## Add My PPA
```
sudo add-apt-repository ppa:danielheth/guid
sudo apt-get update
```

## Installing guid
```
sudo apt-get install guid
```

## Launch Daemon
```
sudo guidd
```

This opens up the 561 tcp port and listens for connections from the client app.  It stays resident so you'll need to open a new terminal window to test the client connecting into it.

## Test Client
```
guid
```

Running this command will reach out to the server on localhost:561 and asks for a truely UUID and exits.


## Uninstall guid
```
sudo apt-get remove guid
```


