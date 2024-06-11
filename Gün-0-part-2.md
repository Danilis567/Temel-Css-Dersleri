## Kutu Modeli (Box Model)

Kutu modeli, web sayfalarında HTML elementlerinin boyutlandırılması ve düzenlenmesi için temel bir kavramdır. Her HTML elementi, içeriği, dolgusu, kenarlığı ve dış boşlukları olan bir kutu olarak düşünülür.

Örnekleri teker teker deneyin kendinize göre küçük değişiklikler yaparak pratik yapın.

### Bileşenler

1. **Kenar Boşlukları (Padding):** İçerik alanıyla içerik sınırı arasındaki alan. Dolgu, içeriğin kutu içindeki konumunu ve boyutunu belirler.

```css
    .padding-box {
        width: 200px;
        height: 200px;
        background-color: #f0f0f0;
        padding: 20px;
    }
```

```html
<div class="padding-box">
    <p>İçerik Alanı</p>
</div>
```

2. **Kenar Çerçevesi (Border):** Kutunun etrafını çevreleyen çizgi. Kenarlık, kutunun sınırlarını belirler ve içeriğini diğer elementlerden ayırır.
```css
    .border-box {
        width: 200px;
        height: 200px;
        background-color: #f0f0f0;
        border: 2px solid black;
    }
```
border bu şekilde yapılabildiği gibi sağ, sol, yukarı ve  aşagıya özel farklı bir border değeri vermek için :
```css
 .border-box{
	 border-top: 2px red soild;
	border-bottom: 2px red soild;
	border-bottom-color: blue;
 }
```
bu şekilde kullanabilirsiniz tabi pek de işlevli bir yol değil ve tek satırda yazılabilir bir kod 
```css
 .border-box{
	 border: 2px 4px;
 }
```
sadece 2 değer verirseniz yukarı ve aşagıya 

```css
 .border-box{
	 border: 2px 1px 4px 10px;
 }
```
dört değer verirseniz saat yönünde olucak şekilde özeleştirebilirsiniz.

3. **Dış Boşluklar (Margin):** Kutunun diğer elementlere olan uzaklığı. Dış boşluklar, elementin sayfa içindeki konumunu belirler.

### Ek Özellikler

1. **Border Radius:** Kenar köşelerinin yuvarlatılmasını sağlar. Bu özellik, köşeleri düz veya yuvarlak hale getirerek kutuların görünümünü değiştirebilir. Pek anlatılıcak bir yönü yok border-color ve border-style hariç benzer bir kullanımı var.

```css
.rounded-box {
        width: 200px;
        height: 200px;
        background-color: #f0f0f0;
        border: 2px solid #333;
        border-radius: 20px;
    }
```

### Örnek

Aşağıdaki HTML ve CSS kodu, bir kutu örneğini göstermektedir:

```html
<div class="box">
    <p>İçerik Alanı</p>
</div>
```
Bu kodu tüm gösterdiğim özelikleri üstünde deniyerek tekrar edin.



