import socket;

ip1 =int(input('start ip part 1 '))
ip2 =int(input('start ip part 2 '))
ip3 =int(input('start ip part 3 '))
ip4 =int(input('start ip part 4 '))

start_ip = str(ip1) +"."+ str(ip2)+"."+str(ip3)+"."+str(ip4)
print (start_ip)

ip5 = int(input('end ip part 1 '))
ip6 = int(input('end ip part 2 '))
ip7 = int(input('end ip part 3 '))
ip8 = int(input('end ip part 4 '))

end_ip =str(ip5) +"."+ str(ip6)+"."+str(ip7)+"."+str(ip8)

current_ip = start_ip
while (end_ip != current_ip):
        
        if ip4 != 255:
            ip4 = ip4+1
        elif ip4 == 255:
            ip3 = ip3+1
            ip4 =0
        elif ip3 == 255:
            ip2 = ip2+1
            ip3 =0
        elif ip2 == 255:
            ip1 = ip1+1
            ip2 = 0

        current_ip =str(ip1) +"."+ str(ip2)+"."+str(ip3)+"."+str(ip4)
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

        try:
            result = s.connect((current_ip,23))
            print(current_ip +" connected port 23")
        except :
            print(current_ip +' connection error')
        finally:
            s.close()
