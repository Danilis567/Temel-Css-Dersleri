# CSS Seçiciler (Selectors)

CSS seçicileri, HTML elementlerini hedef alarak bu elementlere stil uygulamak için kullanılır. Bu dosyada CSS seçicilerinin en yaygın türlerini ve nasıl kullanıldıklarını inceleyeceğiz.

## Tür Seçiciler (Type Selectors)

Tür seçiciler, doğrudan HTML elementlerinin adını kullanarak bu elementleri seçer.

```css
p {
    color: blue;
}
```

Yukarıdaki CSS kodu, sayfadaki tüm <p> elementlerinin metin rengini mavi yapar.

Tür seçiciler ile belirli bir türdeki HTML elementlerinin tamamını seçip manipüle edebiliriz.

## Sınıf Seçiciler (Class Selectors)

Sınıf seçiciler, belirli bir sınıfa (class) sahip elementleri seçmek için kullanılır. Genellikle aynı stil tanımını birden fazla HTML elementine uygulamak için kullanılır.

#### HTML'de Sınıf Kullanımı

```html
<p class="renk">Merhaba!!</p>
``` 
#### CSS'de Sınıf Tanımlama

```Css
.renk { 
    color: red; 
}
```

Yukarıdaki CSS kodu, class="renk" olan tüm elementlerin metin rengini kırmızı yapar örnekler artırılabilir ama şimdilik bu yeter.

## ID Seçiciler (ID Selectors)

ID seçiciler, belirli bir ID'ye sahip tek bir elementi seçmek için kullanılır. ID seçiciler, diyez işaretini (#) ID adının önüne ekleyerek tanımlanır.

#### HTML'de ID Kullanımı

```html
<p id="baslik">Hoşgeldiniz!</p>
```

#### CSS'de ID Tanımlama

```css
#baslik {
    font-size: 24px;
    font-weight: bold;
}
```

Yukarıdaki CSS kodu, id="baslik" olan elementin yazı boyutunu 24 piksel ve yazı kalınlığını kalın yapar.

## Evrensel Seçiciler (Universal Selectors)

Evrensel seçici, yıldız işareti (*) kullanarak sayfadaki tüm elementleri seçer.


```css
* {
    margin: 0;
    padding: 0;
}
```

Yukarıdaki CSS kodu, sayfadaki tüm elementlerin kenar boşluklarını (margin) ve iç boşluklarını (padding) sıfırlar. Genelikle bunu global bir font atamak yada biraz eski bir tabir olan reset css için kullanırız.


## Grup Seçiciler (Group Selectors)

Grup seçiciler, virgül (,) kullanarak birden fazla seçiciyi bir araya getirir ve hepsine aynı stilleri uygular.

```css
h1, h2, h3 {
    font-family: Arial, sans-serif;
    color: navy;
}
```

Yukarıdaki CSS kodu, <h1>, <h2> ve <h3> elementlerinin yazı tipini Arial ve metin rengini lacivert yapar.
Belirli elemanlara ayrı ayrı aynı özellikleri verip kodu uzatmamızı engelleyen bir özellik.


## Bağlamsal Seçiciler (Descendant Selectors)

Bağlamsal seçiciler, belirli bir hiyerarşideki elementleri seçmek için kullanılır. Bir elementin içindeki belirli elementleri hedef alır.

```html
<div>
    <p>Hii!!</p>
<div/>
```

Bu şekilde belirli bir hiyerarşi içinde çocuk evebeyin düzeni ile seçip manipüle edebiliriz.


```css
div p {
    font-size: 14px;
}
```

Yukarıdaki CSS kodu, sadece bir <div> elementi içinde bulunan <p> elementlerinin yazı boyutunu 14 piksel yapar.

div > p 
kısaca div içinde ki p elemanını al ve ```css font-size: 14px;``` yap diyoruz

#### Çocuk Seçiciler (Child Selectors)

Çocuk seçiciler, belirli bir elementin doğrudan çocuklarını seçer. > sembolü kullanılarak tanımlanır.

```css
ul > li {
    list-style-type: none;
}
```
Yukarıdaki CSS kodu, sadece bir <ul> elementinin doğrudan çocukları olan <li> elementlerinin madde işaretlerini kaldırır.

#### Komşu Kardeş Seçiciler (Adjacent Sibling Selectors)

Komşu kardeş seçiciler, belirli bir elementin hemen yanındaki kardeş elementi seçer. + sembolü kullanılarak tanımlanır.

```css
h1 + p {
    margin-top: 0;
}
```


Yukarıdaki CSS kodu, bir <h1> elementinden hemen sonra gelen <p> elementinin üst kenar boşluğunu sıfırlar.

#### Genel Kardeş Seçiciler (General Sibling Selectors)

Genel kardeş seçiciler, belirli bir elementin tüm kardeş elementlerini seçer. ~ sembolü kullanılarak tanımlanır.

```css
h1 ~ p {
    color: gray;
}
```
Yukarıdaki CSS kodu, bir <h1> elementinin tüm kardeş <p> elementlerinin metin rengini gri yapar.

## Özellik Seçiciler (Attribute Selectors)

Özellik seçiciler, belirli bir özelliğe sahip elementleri seçmek için kullanılır. Köşeli parantezler içinde özellik adı kullanılarak tanımlanır.

```css
a[target="_blank"] {
    color: red;
}
```
Yukarıdaki CSS kodu, target="_blank" özelliğine sahip tüm <a> elementlerinin metin rengini kırmızı yapar.

Bu temel seçici türleri, CSS kullanarak HTML elementlerini hedef almanızı ve stilize etmenizi sağlar. Seçicileri doğru bir şekilde kullanarak web sayfanızın görünümünü ve hissini tamamen kontrol edebilirsiniz.

Şimdilik bunları bilmek yeterli bir kaç pratik ile pekiştirebilirsiniz.
