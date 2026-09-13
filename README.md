# Movie Recommendation System

Python ve Pandas kullanılarak geliştirilmiş, interaktif bir film öneri sistemi. TF-IDF ile film arama ve collaborative filtering (işbirlikçi filtreleme) ile öneri üretme yöntemlerini birlikte kullanır.

## Nasıl Çalışır

1. **Film Arama:** Kullanıcının yazdığı film ismi, `TfidfVectorizer` ile vektöre çevrilir ve `cosine_similarity` kullanılarak en yakın film bulunur.

2. **Öneri Üretme:** Seçilen filme yüksek puan (4 üstü) veren kullanıcılar bulunur. Bu "benzer zevkli" kullanıcıların beğendiği diğer filmler, genel kullanıcı kitlesine kıyasla ne kadar öne çıktığına göre puanlanır ve sıralanır.

3. **Arayüz:** `ipywidgets` ile oluşturulan basit bir metin kutusuna film adı yazıldıkça, öneriler anlık olarak güncellenir.

## Kullanılan Kütüphaneler

- pandas
- scikit-learn
- ipywidgets
- numpy

## Veri Seti

Bu proje MovieLens veri setini kullanır.

- movies.csv — bu repoda mevcut.
- ratings.csv — dosya boyutu nedeniyle repoya eklenmemiştir. Kullanmak için MovieLens sitesinden uygun veri setini indirip proje klasörüne ratings.csv olarak eklemeniz gerekir.

## Kurulum ve Çalıştırma

1. Bu repoyu klonlayın veya indirin.
2. ratings.csv dosyasını MovieLens'ten indirip proje klasörüne ekleyin.
3. Gerekli kütüphaneleri kurun: pip install pandas scikit-learn ipywidgets numpy
4. film_onerici.ipynb dosyasını Jupyter Notebook veya VS Code'da açıp hücreleri sırasıyla çalıştırın.
5. Açılan metin kutusuna bir film adı yazarak benzer film önerilerini görün.

## Örnek

"Moonlight" filmi arandığında, benzer temalı dramalar önerilir: Eternal Sunshine of the Spotless Mind, The Shining, 2001: A Space Odyssey gibi.
