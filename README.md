# Grafana 
# how to install grafana
     sudo apt-get install -y apt-transport-https
     sudo apt-get install -y software-properties-common wget

# २. Grafana GPG की डाउनलोड करणे (Downloading Grafana GPG Key)

     sudo wget -q -O /usr/share/keyrings/grafana.key https://apt.grafana.com/gpg.key
     
# ३. Grafana APT रिपॉजिटरी जोडणे (Adding the Grafana APT Repository)

     echo "deb [signed-by=/usr/share/keyrings/grafana.key] https://apt.grafana.com stable main" | sudo tee /etc/apt/sources.list.d/grafana.list

# ४. रिपॉजिटरी अपडेट करणे आणि Grafana इन्स्टॉल करणे (Updating and Installing Grafana)

     sudo apt-get update
     sudo apt-get install grafana -y

# 5 Starte the grafana

     sudo systemctl start grafana-server

     sudo systemctl enable grafana-server

     sudo systemctl status grafana-server

