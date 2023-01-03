Since I heard that KrakenD (the API gateway) has better performance in term of speed when compare to Kong and Tyk. That's why I'm interested to try using it. I started to findout about:

- How to deploy KrakenD?
- KrakenD Configuration and file formats.
- KrakenD Configuration using tool named 'KrakenDesigner'.
- Pros & Cons of using KrakenD.


## Deployment and Configuration KrakenD

### TL; DR

```
$ docker-compose up -d

$ curl http://127.0.0.1/

$ curl http://127.0.0.1/ip

$ curl http://127.0.0.1/aggs
```


### Check config file

```
$ docker-compose up check
Starting krakend_check_1 ... done
Attaching to krakend_check_1
check_1     | Parsing configuration file: krakend.yml
check_1     | Syntax OK!
krakend_check_1 exited with code 0
```

### Start Designer

```
docker-compose up -d designer
```

### Start KrakenD

```
docker-compose up -d krakend
```

## Conclusion:
- It is easy to deploy KrakenD (after transform .json config file from long to short one. //just my preference)
- KrakenD support many config file formats e.g. .json (Recommended), .toml, .yaml, etc.
- KrakenD do cares about the performance most, that's why there is no reload config.
- There is a tool, KrakenDesigner to help user create config file in .json format.
- In my opinion, the impressive feature of KrakenD is 'aggregate API' (there is no such thing for Kong)
