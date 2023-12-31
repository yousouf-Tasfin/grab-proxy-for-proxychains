# grab-proxy-for-proxychains


#grab proxy http,socks5,socks4

curl --location 'https://api.proxyscrape.com/v2/?request=displayproxies&protocol=http&timeout=400&country=all&ssl=all&anonymity=all' | tee grab

#check working alive proxy from: 

https://proxyscrape.com/online-proxy-checker

#print for proxy chain format. change socks5 for with your protocol

cat alive.txt | awk -F: '{print "socks5 " $1, $2}'

#edit proxychain conf

nano /etc/proxychains4.conf

done 
