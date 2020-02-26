import cv2
import numpy as np

kamera=cv2.VideoCapture(0)
#kamera.set(3,300)#KAMERANIN BOYUTUNU DÜZENLERİZ
#kamera.set(10,300)
def ayarlama(kare,yuzde=50):#KAMERANIN BOYUTUNU AYARLAMA
    genislik=int(kare.shape[1]*yuzde/100)#YUKSEKLİK BİRİNCİSİ 
    yukseklik=int(kare.shape[0]*yuzde/100)#EN İKİNCİSİ 
    boyut=(genislik,yukseklik)
    return cv2.resize(kare,boyut,interpolation=cv2.INTER_AREA)
while True:
    ret,kare=kamera.read()
    gri=cv2.cvtColor(kare,cv2.COLOR_BGR2GRAY)
    
    kare1=ayarlama(kare)
    cv2.imshow("Griton",gri) 
    cv2.imshow("Video",kare)
    cv2.imshow("Video1",kare1) 
    if cv2.waitKey(25) & 0xFF==ord('q'):
        break
kamera.release()
cv2.destroyAllWindows()

     

