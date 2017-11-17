# Encryption
class Cod: 
    def __init__(self,n,k): 
        self.n = n 
        self.k = k 

    def encode(self): 
        for i in self.n: 
            if (ord(i) in range(65, 90-self.k+1)) or (ord(i) in range (97, 122 - self.k+1)) : 
                ch = ord(i)
                ch = ch + self.k 
            else: 
                ch = ord(i)-26+self.k 
            print(chr(ch)) 

    def decode(self): 
        for i in self.n: 
            if (ord(i) in range (65 +self.k, 91)) or (ord(i) in range(97 + self.k, 123)): 
                ch = ord(i) 
                ch = ch - self.k 
            else: 
                ch = ord(i)+26-self.k 
            print(chr(ch)) 

per = Cod("defDEFabcABC",3) 
per.decode()
