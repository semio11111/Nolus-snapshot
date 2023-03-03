# Nolus-snapshot

```
sudo systemctl stop nolusd

cp $HOME/.nolus/data/priv_validator_state.json $HOME/.nolus/priv_validator_state.json.backup

wget http://65.108.129.29:8000/nolusdata.tar.gz 
tar -C $HOME/ -zxvf nolusdata.tar.gz --strip-components 1

mv $HOME/.nolus/priv_validator_state.json.backup $HOME/.nolus/data/priv_validator_state.json

sudo systemctl start nolusd && sudo journalctl -u nolusd -f --no-hostname -o cat
```
