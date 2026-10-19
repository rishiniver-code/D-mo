import socket
import requests

def get_local_ip():
    s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
    try:
        s.connect(("8.8.8.8", 80))
        ip = s.getsockname()[0]
    except Exception:
        ip = "127.0.0.1"
    finally:
        s.close()
    return ip

def get_public_ip():
    r = requests.get("https://api.ipify.org", timeout=10)
    return r.text.strip()

print("Local IP :", get_local_ip())
print("Public IP:", get_public_ip())
