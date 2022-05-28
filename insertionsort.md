# Insertion Sort

Insertion Sort dizi elemanlarını bir alt dizi oluşturarak sıralar. `[22,27,16,2,18,6]`  şeklinde bir dizinin Insertion Sort ile sıralanışını yapalım.


1. Dizinin ilk elemanı alınır ve sıralı alt dizinin ilk elemanı olarak yerleştirilir. Alt dizide sadece 1 eleman olduğundan sıralıdır.

2. Dizinin sonraki elemanı seçilir, alt dizinin ilk elemanıyla karşılaştırılır. Eğer orijinal dizinin elemanı ilk elemandan küçükse dizinin sol tarafına alınır, değilse sağ tarafına alınır.

3. Dizinin geri kalan elemanları da seçilir, alt dizinin elemanlarıyla kıyaslanır ve alt dizide 2. adımdaki kıyas işlemine göre uygun konuma yerleştirilir.

4. Geriye kalan son eleman da alt dizide uygun konuma yerleştirilir. Böylelikle alt dizi oluşturulur.

| Orijinal Dizi | Alt Dizi |
| ----------- | ----------- |
| [**22**,27,16,2,18,6 ]| [**22**]| |
| [22,**27**,16,2,18,6 ]   | [**22**,**27**]   |
| [22,27,**16**,2,18,6 ]   | [**16**,**22**,**27**]|
| [22,27,16,**2**,18,6 ]   | [**2**,**16**,**22**,**27**]|
| [22,27,16,2,**18**,6 ]   | [**2**,**16**,**18**,**22**,**27**]|
| [22,27,16,2,18,**6** ]   | [**2**,**6**,**16**,**18**,**22**,**27**]|


## Big-O Gösterimi

 n orijinal dizinin eleman sayısı olmak üzere orijinal dizideki her bir adım için alt dizide n-1 adım gerçekleşir.

Dizi zaten sıralı haldeyse karşılaştırmalar için (**best-case**) : $T_{n}=O(n)$ yer değiştirmeler için: $T_{1}=O(1)$

Dizi ters sıralı (**worst-case**) veya rastgele sıralı ise (**average-case**):

$\sum_{i=1}^{n} (n-1) = (n-1)(n-1+1)/2 $

$T_{n}=O(n^2)$
