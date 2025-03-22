---
creation date: <% tp.file.creation_date() %>
---

> [!Notes] Setup Documentation
> https://dashboard.ngrok.com/get-started/setup/linux

Install ngrok via Apt with the following command:
```
curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
	| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \
	&& echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
	| sudo tee /etc/apt/sources.list.d/ngrok.list \
	&& sudo apt update \
	&& sudo apt install ngrok
```
 
Run the following command to add your authtoken to the default **ngrok.yml** [configuration file](https://ngrok.com/docs/agent/config/).
```
ngrok config add-authtoken 2uaQPOSf3fk8o4fg42LrP9rCehV_31HZYyKBdBGgPZxJk8Dja
```


### Deploy NGROK

Put your app online at an [ephemeral domain](https://ngrok.com/docs/network-edge/domains-and-tcp-addresses/#ephemeral-domains) forwarding to your upstream service. For example, if it is listening on port `http://localhost:8080`, run:
```
ngrok http http://localhost:3000
```


Link to original: [[2025-03-20]]