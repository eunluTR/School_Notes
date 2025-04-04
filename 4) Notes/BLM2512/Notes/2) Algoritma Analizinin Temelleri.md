
Time: 04-04-2025 14.04

Tags: [[BLM2512]]

# Algoritma Analizi

## 1. Zaman Karmaşıklığı (Time Complexity)
- Algoritmanın çalışma süresinin, girilen verinin boyutu ve yapısına bağlı olarak değerlendirilmesi.
### a) Girdi Sayısı (Number of Input)
- İşlenecek verinin miktarı arttıkça algoritmanın süresi nasıl değişir, bunu inceler.
### b) Girdi Türü (Type of Input)
- Veri sıralı mı, rastgele mi, ya da özel bir yapıya mı sahip gibi durumların algoritma performansına etkisini inceler.

## 2. Bellek Karmaşıklığı (Space Complexity)
- Algoritmanın çalışırken kullandığı ek bellek alanının analiz edilmesidir.

## Temel İşlemler (Basic Operations)
- Algoritmanın adımlarında sıkça gerçekleşen basit işlemlerdir. Her biri 1 adım olarak değerlendirilir.
  - **Atama (Assignment)**: Bir değerin değişkene atanması.
  - **Aritmetik İşlem (Arithmetic Operation)**: Toplama, çıkarma gibi matematiksel işlemler.
  - **Karşılaştırma İşlemi (Comparison Operation)**: İki değerin karşılaştırılması.
  - **Değişken Tanımlama (Variable Declaration)**: Yeni bir değişkenin bellek alanında tanımlanması.

```C
int i, m = 1, n;
for (i = 0, i < n, i + 1)
	m = i * m;

| Operation             | Frequency  |
| --------------------- | ---------- |
| Variable Decleration  |     3      |
| Assignment            |   n + 2    |
| Less Than Comparision |   n + 1    |
| Increment             |     n      |
| Multiplication        |     n      |
|   Total:              |   4n + 6   |
```

## Linear ve Min-Max Algoritma Performanslarının Karşılaştırılması:

| Algoritma          | Varyasyon | Best Case                          | Average Case                       | Worst Case                           | Big-O Notasyonu Açıklaması                                               |
| ------------------ | --------- | ---------------------------------- | ---------------------------------- | ------------------------------------ | ------------------------------------------------------------------------ |
| **Linear Search**  | Unsorted  | Hedef ilk elemanda bulunur. O(1)   | Hedef rastgele yerde bulunur. O(n) | Hedef son elemanda veya yoktur. O(n) | İşlem sayısı veri boyutu (n) ile doğru orantılıdır.                      |
| **Linear Search**  | Sorted    | Hedef ilk elemanda bulunur. O(1)   | Hedef rastgele yerde bulunur. O(n) | Hedef son elemanda veya yoktur. O(n) | Veri sıralı olsa bile linear search ortalama O(n) sürer.                 |
| **Min-Max Search** | Unsorted  | Tüm elemanlar kontrol edilir. O(n) | Tüm elemanlar kontrol edilir. O(n) | Tüm elemanlar kontrol edilir. O(n)   | En büyük ve en küçük eleman için her durumda tüm veriler kontrol edilir. |
| **Min-Max Search** | Sorted    | İlk ve son eleman alınır. O(1)     | İlk ve son eleman alınır. O(1)     | İlk ve son eleman alınır. O(1)       | Veriler sıralı olduğundan en iyi durum gerçekleşir.                      |

## 5. Fonksiyon Büyüme Hızı (Function Growth Rate)
- Algoritmaların büyüme oranlarını karşılaştırırken kullanılır:
  - Sabit değer < Logaritmik < Doğrusal < Doğrusal-logaritmik < Karesel < Kübik < Üssel < Faktöriyel
  - `1 < log n < n < n log n < n² < n³ < 2ⁿ < n!`

## 6. Asimptotik Gösterimler (Asymptotic Notation)
- Algoritmaların büyüme hızını karşılaştırmak için kullanılan matematiksel gösterimler:
  - **Big O (O)**: Algoritmanın en kötü durumdaki üst sınırını belirtir.
  - **Big Theta (Θ)**: Algoritmanın ortalama durumdaki sınırını belirtir (üst ve alt sınır).
  - **Big Omega (Ω)**: Algoritmanın en iyi durumdaki alt sınırını belirtir.
![[Asymptoyic-Notations.png.webp]]

## 7. Ampirik Analiz (Empirical Analysis)
- Algoritmanın performansını teorik olarak değil, gerçek veri setleri üzerinde uygulayıp ölçüm yaparak değerlendirilmesidir.
- Algoritmaların pratikteki davranışını anlamak için kullanılır.

# References
