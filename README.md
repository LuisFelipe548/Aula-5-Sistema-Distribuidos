# Aula-5-Sistema-Distribuidos

Codigo corrida.py

import threading
import time

saldo = 1000

def sacar(valor):
    global saldo

    saldo_atual = saldo
    time.sleep(0.01)
    saldo = saldo_atual - valor

threads = []

for i in range(10):
    t = threading.Thread(target=sacar, args=(50,))
    threads.append(t)
    t.start()

for t in threads:
    t.join()

print("Saldo esperado: 500")
print("Saldo obtido:", saldo)

resultado: Saldo esperado: 500
Saldo obtido: 950
PS C:\Users\aluno\Desktop\Aula5> ^C
PS C:\Users\aluno\Desktop\Aula5> 
PS C:\Users\aluno\Desktop\Aula5>  c:; cd 'c:\Users\aluno\Desktop\Aula5'; & 'C:\Program Files\Python313\python.exe' 'c:\Users\aluno\.vscode\extensions\ms-python.debugpy-2026.6.0-win32-x64\bundled\libs\debugpy\launcher' '49285' '--' 'C:\Users\aluno\Desktop\Aula5\corrida.py' 
Saldo esperado: 500
Saldo obtido: 900
PS C:\Users\aluno\Desktop\Aula5> ^C
PS C:\Users\aluno\Desktop\Aula5> 
PS C:\Users\aluno\Desktop\Aula5>  c:; cd 'c:\Users\aluno\Desktop\Aula5'; & 'C:\Program Files\Python313\python.exe' 'c:\Users\aluno\.vscode\extensions\ms-python.debugpy-2026.6.0-win32-x64\bundled\libs\debugpy\launcher' '49454' '--' 'C:\Users\aluno\Desktop\Aula5\corrida.py' 
Saldo esperado: 500
Saldo obtido: 950
PS C:\Users\aluno\Desktop\Aula5> 
