# ALPHA_N-118

#the project python program


import requests

response = requests.get('http://3124-2409-4063-4b0b-9605-9c03-b60-1870-cbd7.ngrok.io')
print(response.status_code)
print(response.json())

HR= response.json()['Heart Rate']
BO= response.json()['SPO2']
SL= response.json()['Stress Level']

p=59
if HR<=p:
    import pywhatkit
    import datetime
    now= datetime.datetime.now()
    H=now.hour
    S=now.minute
    M= S + 2
    pywhatkit.sendwhatmsg('+917755880042','SOS please Check your friend Munish his Heart Rate are not good',H,M)

elif HR>p:

    q=89
    if BO<=q:
     import pywhatkit
     import datetime
     now= datetime.datetime.now()
     H=now.hour
     S=now.minute
     M= S + 2
     pywhatkit.sendwhatmsg('+917755880042','SOS please Check your friend Munish his SPO2 is not good',H,M)

    elif BO > p:

        r = 76
        if SL > r:
            import pywhatkit
            import datetime

            now = datetime.datetime.now()
            H = now.hour
            S = now.minute
            M = S + 2
            pywhatkit.sendwhatmsg('+917755880042', 'SOS please Check your friend Munish he is having stress', H
