import socket

def simple_port_scanner(target, ports):
    print(f"Scanning {target}...")
    for port in ports:
        sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        sock.settimeout(1)  # 1-second timeout
        result = sock.connect_ex((target, port))
        if result == 0:
            print(f"[+] Port {port} is OPEN")
        else:
            print(f"[-] Port {port} is CLOSED or FILTERED")
        sock.close()

# Example usage
target_ip = "192.168.1.16"
ports_to_check = [21, 22, 23, 80, 443]
simple_port_scanner(target_ip, ports_to_check)
