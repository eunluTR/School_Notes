
Time: 04-04-2025 15.04

Tags: [[BLM2512]]

# Recursion vs. Iteration 

| Özellik              | **Recursion**                                     | **Iteration**                                    |
| -------------------- | ------------------------------------------------- | ------------------------------------------------ |
| Tanım                | Fonksiyonun kendisini çağırmasıdır.               | Bir komut setinin döngülerle tekrar edilmesidir. |
| Yapı                 | Fonksiyon çağrıları (Functions)                   | Döngüler (Loops)                                 |
| Sonlanma Durumu      | Temel Durum (Base Condition)                      | Koşul (Condition)                                |
| Kod Uzunluğu         | Daha küçük kod boyutu                             | Daha büyük kod boyutu                            |
| Zaman Karmaşıklığı   | Yüksek (High time complexity)                     | Düşük (Low time complexity)                      |
| Bellek Karmaşıklığı  | Yüksek (High space complexity)                    | Düşük (Low space complexity)                     |
| Hız                  | Yavaş (Slow speed)                                | Hızlı (Fast speed)                               |
| Sonsuz Tekrar Durumu | Stack Overflow hatası (Infinite repetition crash) | Sonsuz döngü (Infinite loop)                     |

## DFS (Derinlik Öncelikli Arama) Mantığı
---
- **Başlangıç:** Belirtilen başlangıç düğümü (startVertex) ile başlar.
- **Ziyaret İşareti:** Ziyaret edilen düğümü işaretlemek için `visited` dizisi kullanılır.
- **Rekursif Çağrı:** Yardımcı fonksiyon (örneğin, `dfsUtil`) çağrılarak, geçerli düğümün tüm komşuları üzerinde (yani, grafiğin satırındaki 1 değerlerine sahip olan düğümler) yine aynı işlem uygulanır.
- **Sıralama:** Önce derinlere inilir, yani bir düğümün tüm alt düğümleri ziyaret edilmeden diğer düğümlere geçilmez.
- **Stack Kullanımı:** Fonksiyon çağrıları yerel çağrı yığınına (stack) atılır. Çok derin graf yapılarında bu, stack overflow hatasına yol açabilir.

```C
void DFS(int startVertex) {
    int visited[100] = {0};
    int graph[100][100] = {
        {0, 1, 1, 0, 0},
        {1, 0, 0, 1, 0},
        {1, 0, 0, 1, 1},
        {0, 1, 1, 0, 0},
        {0, 0, 1, 0, 0}
    };
    int vertices = 5;

    void dfsUtil(int vertex) {
        visited[vertex] = 1;
        printf("%d ", vertex);

        for(int i = 0; i < vertices; ++i) {
            if(graph[vertex][i] && !visited[i]) {
                dfsUtil(i);
            }
        }
    }

    dfsUtil(startVertex);
}
```

## BFS (Genişlik Öncelikli Arama) Mantığı
---
- **Başlangıç:** Belirtilen başlangıç düğümü `visited` dizisine işaretlenir ve kuyruk yapısına eklenir.
- **Kuyruk Yapısı:** FIFO (First-In-First-Out) prensibiyle çalışan kuyruk sayesinde, önce eklenen düğümler işlenir.
- **Düğüm İşleme:** Kuyruktan bir düğüm çıkarılır (dequeue) ve ekrana yazdırılır.
- **Komşuların Kuyruğa Eklenmesi:** Çıkarılan düğümün komşuları kontrol edilir; eğer henüz ziyaret edilmediyse, ziyaret edilir (işaretlenir) ve kuyruğa eklenir.
- **Sıralama:** Bu yöntem, grafiğin her seviyesini sırayla işler; yani, başlangıç düğümüne yakın olan düğümler önce ziyaret edilir.
- **Sonsuz Döngü Riski:** Eğer çıkış koşulu (kuyruğun boş olması) doğru ayarlanmazsa sonsuz döngüye girme riski vardır.

```C
void BFS(int startVertex) {
    int visited[100] = {0};
    int graph[100][100] = {
        {0, 1, 1, 0, 0},
        {1, 0, 0, 1, 0},
        {1, 0, 0, 1, 1},
        {0, 1, 1, 0, 0},
        {0, 0, 1, 0, 0}
    };
    int queue[100];
    int front = -1, rear = -1;
    int vertices = 5;

    void enqueue(int vertex) {
        queue[++rear] = vertex;
    }

    int dequeue() {
        return queue[++front];
    }

    int isEmpty() {
        return front == rear;
    }

    visited[startVertex] = 1;
    enqueue(startVertex);

    while(!isEmpty()) {
        int currentVertex = dequeue();
        printf("%d ", currentVertex);

        for(int i = 0; i < vertices; ++i) {
            if(graph[currentVertex][i] && !visited[i]) {
                visited[i] = 1;
                enqueue(i);
            }
        }
    }
}
```

## Toplama Operatörü Kullanarak Çarpma İşlemi Yapan Rekursif Fonksiyon
---
```C
int multiply(int a, int b) {
	if(b == 0)
        return 0;
    return a + multiply(a, b - 1);
}
```

# References
