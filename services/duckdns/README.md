# DuckDNS

1. Rename `duck.example.sh` to `duck.sh` and update `<domain>` and `<token>` with values from duckdns.org

2. Ensure `duck.sh` is executable.
	```sh
	chmod 700 duck.sh
	```
3. Set Up Cron Job
	```sh
	crontab -e
	```
	Paste at the bottom:
	```
	*/5 * * * * ~/duckdns/duck.sh >/dev/null 2>&1
	```
	This will ensure that `duck.sh` will run every 5 minutes.


