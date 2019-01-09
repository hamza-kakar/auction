## start the network (discarding old data)

cd fabric-dev-servers
```
./startFabric.sh
```

go to auction folder

### import .bna file
go to generated folder named auction 
```
composer network install --card PeerAdmin@hlfv1 --archiveFile auction@0.0.6.bna
```

### start network

```
composer network start --networkName auction --networkVersion 0.0.6 --networkAdmin admin --networkAdminEnrollSecret adminpw --card PeerAdmin@hlfv1
```


### run rest server 
```
composer-rest-server -c admin@auction
```


-----------------------------------------------------------------------------------

## start the network (keeping old data)

cd fabric-dev-servers/fabric-scripts/hlfv11/composer/
```
docker-compose start
```

go to auction folder

### run rest server 
```
composer-rest-server -c admin@auction
```