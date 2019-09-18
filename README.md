# mendefenisikan kelas induk pertama
clas Induk1(object):
  def __init__(self,a):
    self.a=a
   def cetakA(self):
    print("Nilai a=",self.a)
    
# mendefenisikan kelas induk kedua 
  class Induk2(object):
    def __init__(self,b):
      self.b=b
    def cetakB(self):
      print("Nilai b=",self.b)
      
# mendefenisikan kelas turunan
  class Anak(induk1,induk2):
    def __init__(self,a,b,c):
      # memanggil induk1.__init__()
      induk1.__init__(self,a)
      # memanggil Induk2.__init__()
      induk2.__init__(self,b)
      self.c=c
     def cetakC(self):
      print("Nilai c=",self.c)
      
def main():
  # membuat objek dari kelas Anak
  obj=Anak(111,222,333)
  
  # memanggil metode kelas Induk2 dari obj
  obj.cetakB()
  
  # memanggil metode kelas Anak
  obj.cetakC()
  
if __name__=="__main__":
  main()
