<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Self Kuaför - Yardım Dokümanı</title>
    <style>
        :root {
            --primary-color: #4a6fc7;
            --secondary-color: #f8f9fa;
            --accent-color: #6c5ce7;
            --text-color: #333;
            --light-gray: #f1f3f5;
            --border-color: #e9ecef;
            --success-color: #23d160;
            --warning-color: #ffdd57;
            --danger-color: #ff3860;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--text-color);
            line-height: 1.6;
            background-color: #fcfcfc;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 2rem 0;
            margin-bottom: 2rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        header .logo-container {
            text-align: right;
            margin-bottom: 10px;
        }
        
        header .logo-link {
            color: white;
            text-decoration: none;
            font-size: 0.9rem;
            opacity: 0.8;
            transition: opacity 0.3s;
        }
        
        header .logo-link:hover {
            opacity: 1;
        }
        
        h1, h2, h3, h4 {
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        h1 {
            font-size: 2.5rem;
            text-align: center;
            color: white;
            margin-bottom: 0.5rem;
        }
        
        h2 {
            font-size: 1.8rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--border-color);
            margin-top: 2rem;
            margin-bottom: 1.5rem;
        }
        
        h3 {
            font-size: 1.4rem;
            margin-top: 1.5rem;
        }
        
        p {
            margin-bottom: 1rem;
        }
        
        a {
            color: var(--accent-color);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        a:hover {
            color: var(--primary-color);
            text-decoration: underline;
        }
        
        ul, ol {
            padding-left: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        li {
            margin-bottom: 0.5rem;
        }
        
        .nav-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 1.5rem;
            margin-bottom: 2rem;
        }
        
        .toc {
            list-style-type: none;
            padding-left: 0;
        }
        
        .toc li {
            margin-bottom: 0.8rem;
        }
        
        .toc a {
            display: block;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s;
        }
        
        .toc a:hover {
            background-color: var(--light-gray);
            text-decoration: none;
            transform: translateX(5px);
        }
        
        .section {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 2rem;
            margin-bottom: 2rem;
        }
        
        .section:target {
            animation: highlight 1.5s ease-out;
        }
        
        @keyframes highlight {
            0% { background-color: rgba(108, 92, 231, 0.2); }
            100% { background-color: white; }
        }
        
        .card {
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
        }
        
        .tip {
            background-color: rgba(35, 209, 96, 0.1);
            border-left: 4px solid var(--success-color);
            padding: 1rem;
            margin-bottom: 1.5rem;
            border-radius: 0 5px 5px 0;
        }
        
        .warning {
            background-color: rgba(255, 221, 87, 0.1);
            border-left: 4px solid var(--warning-color);
            padding: 1rem;
            margin-bottom: 1.5rem;
            border-radius: 0 5px 5px 0;
        }
        
        .note {
            background-color: rgba(108, 92, 231, 0.1);
            border-left: 4px solid var(--accent-color);
            padding: 1rem;
            margin-bottom: 1.5rem;
            border-radius: 0 5px 5px 0;
        }
        
        .img-container {
            text-align: center;
            margin: 1.5rem 0;
        }
        
        .img-container img {
            max-width: 100%;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .img-container img:hover {
            transform: scale(1.01);
        }
        
        .feature {
            display: flex;
            margin-bottom: 1rem;
            align-items: center;
        }
        
        .feature-icon {
            min-width: 30px;
            margin-right: 10px;
            color: var(--accent-color);
            font-size: 1.2rem;
        }
        
        footer {
            background-color: var(--secondary-color);
            padding: 2rem 0;
            text-align: center;
            margin-top: 3rem;
            border-top: 1px solid var(--border-color);
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
            margin-top: 1rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
        }
        
        .contact-icon {
            margin-right: 0.5rem;
            color: var(--primary-color);
        }
        
        .scroll-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: var(--primary-color);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            opacity: 0;
            transition: opacity 0.3s, transform 0.3s;
            transform: translateY(20px);
        }
        
        .scroll-top.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .scroll-top:hover {
            background-color: var(--accent-color);
        }
        
        .panel-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .panel {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            padding: 1.5rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .panel:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .panel-header {
            font-weight: 600;
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 0.5rem;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .panel-grid {
                grid-template-columns: 1fr;
            }
        }

        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            font-weight: 500;
            transition: background-color 0.3s, transform 0.3s;
            margin-top: 1rem;
        }
        
        .cta-button:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
            text-decoration: none;
            color: white;
        }
        
        .emoji {
            margin-right: 5px;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="logo-container">
                <a href="http://istek.softmedyazilim.com/" class="logo-link">Softmed İstekler</a>
            </div>
            <h1>Self Kuaför - Yardım Dokümanı</h1>
            <p style="text-align: center; color: white;">Merhaba! Bu dokümanda Self Kuaför web uygulamasının kullanımıyla ilgili tüm önemli bilgilere ulaşabilirsiniz.</p>
        </div>
    </header>

    <div class="container">
        <div class="nav-card" id="içindekiler">
            <h2>İçindekiler</h2>
            <ul class="toc">
                <li><a href="#başlangıç">🚀 Başlangıç</a></li>
                <li><a href="#kullanıcı-girişi">🔑 Kullanıcı Girişi</a></li>
                <li><a href="#ana-sayfa-ve-modüller">🏠 Ana Sayfa ve Modüller</a></li>
                <li><a href="#müşteri-yönetimi">👥 Müşteri Yönetimi</a></li>
                <li><a href="#randevu-yönetimi">📅 Randevu Yönetimi</a></li>
                <li><a href="#hizmet-ve-personel-yönetimi">💇 Hizmet ve Personel Yönetimi</a></li>
                <li><a href="#fatura-işlemleri">📝 Fatura İşlemleri</a></li>
                <li><a href="#kasa-hareketleri">💰 Kasa Hareketleri</a></li>
                <li><a href="#stok-takibi">📦 Stok Takibi</a></li>
                <li><a href="#raporlama-ve-dışa-aktarma">📊 Raporlama ve Dışa Aktarma</a></li>
                <li><a href="#ayarlar-ve-tanımlar">⚙️ Ayarlar ve Tanımlar</a></li>
                <li><a href="#iletişim">📞 İletişim</a></li>
            </ul>
        </div>

        <div class="section" id="başlangıç">
            <h2>🚀 Başlangıç</h2>
            <ol>
                <li>Web adresi: <a href="https://app.selfkuafor.com/" target="_blank">https://app.selfkuafor.com/</a></li>
                <li>Giriş ekranı üzerinden kullanıcı adı ve şifrenizle sisteme erişin.</li>
                <li>İlk ayarlarınızı yaparak kullanıma başlayın.</li>
            </ol>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_1.png" alt="Giriş Ekranı">
            </div>
        </div>

        <div class="section" id="kullanıcı-girişi">
            <h2>🔑 Kullanıcı Girişi</h2>
            <ul>
                <li>Kayıtlı kullanıcılar giriş yapabilir.</li>
                <li>Şifresini unutanlar "Şifremi Unuttum" seçeneğiyle şifre sıfırlayabilir.</li>
            </ul>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_2.png" alt="Kullanıcı Girişi">
            </div>
        </div>

        <div class="section" id="ana-sayfa-ve-modüller">
            <h2>🏠 Ana Sayfa ve Modüller</h2>
            <p>Giriş yaptıktan sonra, kullanıcılar ana kontrol paneline yönlendirilir. Bu panelde, randevu takvimi, müşteri listesi, Faturalar, Stoklar ve hizmet seçenekleri gibi temel bileşenlere erişim sağlanır.</p>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_3.png" alt="Ana Sayfa ve Modüller">
            </div>
        </div>

        <div class="section" id="müşteri-yönetimi">
            <h2>👥 Müşteri Yönetimi</h2>
            <ul>
                <li>Yeni müşteri ekleyin: Ad, iletişim bilgileri, notlar.</li>
                <li>Profil görüntüleme: Geçmiş randevular ve notlar.</li>
            </ul>
            
            <div class="tip">
                <p><strong class="emoji">💡</strong> <strong>İpucu:</strong> Müşteri adında arama yaparken büyük/küçük harf duyarlılığı yoktur.</p>
            </div>
            
            <div class="tip">
                <p><strong class="emoji">💡</strong> <strong>İpucu:</strong> Müşteri adına göre arama yaparak geçmişte eklenmiş kayıtlara hızla ulaşabilirsiniz.</p>
            </div>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_4.png" alt="Müşteri Yönetimi">
            </div>
            
            <h3>Yeni Müşteri Kayıt Ekranı</h3>
            <ol>
                <li>Ana menüden "Müşteriler" sekmesine tıklayın.</li>
                <li>"Yeni Müşteri" butonuna tıklayın.</li>
                <li>Açılan formda Ad, Soyad, Telefon, E-posta gibi bilgileri doldurun.</li>
                <li>Kaydet butonuna tıklayarak müşteriyi ekleyin.</li>
            </ol>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_1.png" alt="Yeni Müşteri Ekranı 1">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_2.png" alt="Yeni Müşteri Ekranı 2">
            </div>
            
            <h3>Müşteri Takibi</h3>
            <p>Müşteri takibi, bir işletmenin müşterilerle satış sonrası etkileşimlerini düzenli ve stratejik bir şekilde yönetmesidir. Amacı, müşteri memnuniyetini artırmak, ilişkileri güçlendirmek ve uzun vadeli sadakat oluşturmaktır.</p>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_3.png" alt="Müşteri Takibi 1">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_4.png" alt="Müşteri Takibi 2">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_5.png" alt="Müşteri Takibi 3">
            </div>
        </div>

        <div class="section" id="randevu-yönetimi">
            <h2>📅 Randevu Yönetimi</h2>
            
            <h3>Yeni Randevu Oluşturma</h3>
            <p>Kullanıcılar, tarih ve saat seçerek yeni randevular oluşturabilirler.</p>
            <ol>
                <li>"Randevular" sekmesine girin.</li>
                <li>Takvimde ilgili tarihi seçin.</li>
                <li>Açılan pencerede müşteri, hizmet, personel ve saat bilgilerini girin.</li>
                <li>"Kaydet" ile randevuyu oluşturun.</li>
            </ol>
            
            <h3>Mevcut Randevuları Düzenleme/İptal Etme</h3>
            <p>Mevcut randevular, ihtiyaçlara göre düzenlenebilir veya iptal edilebilir.</p>
            <ul>
                <li>Mevcut bir randevunun üzerine tıklayarak tarih, saat veya müşteri bilgilerini değiştirebilir ya da randevuyu iptal edebilirsiniz.</li>
                <li>Takvim görünümü: Günlük, haftalık, aylık</li>
            </ul>
            
            <div class="warning">
                <p><strong class="emoji">⚠️</strong> <strong>Not:</strong> Randevular çakışmalara karşı sistem tarafından otomatik kontrol edilir.</p>
            </div>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_5.png" alt="Randevu Takvimi 1">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_6.png" alt="Randevu Takvimi 2">
            </div>
        </div>

        <div class="section" id="hizmet-ve-personel-yönetimi">
            <h2>💇 Hizmet ve Personel Yönetimi</h2>
            
            <ul>
                <li>Hizmet tanımlanabilir ve yeni hizmet eklenebilir.</li>
                <li>Yeni hizmet ekleme, güncelleme ve silme işlemleri kolayca yapılabilir.</li>
            </ul>
            
            <h3>Yeni Hizmet Ekleme</h3>
            <p>Girilmesi gereken bilgiler:</p>
            <ul>
                <li>Hizmet Adı (Örn: Saç Kesimi, Sakal Kesimi, Manikür, Cilt Bakımı)</li>
                <li>Fiyat</li>
                <li>Açıklama/Bilgilendirme Notu</li>
            </ul>
            
            <h3>Hizmet Güncelleme ve Silme</h3>
            <p>Tanımlanmış hizmetler daha sonra fiyat güncellemesi, süre değişikliği veya kaldırma işlemiyle kolayca yönetilebilir.</p>
        </div>

        <div class="section" id="fatura-işlemleri">
            <h2>📝 Fatura İşlemleri</h2>
            
            <p>Faturalandırma sürecini dijitalleştirerek hızlı işlem yapılmasını sağlar. Müşteri bazlı fatura takibi yapılabilir.</p>
            
            <ol>
                <li>Randevu tamamlandıktan sonra ödeme ekranına geçin.</li>
                <li>Alınan hizmet(ler) otomatik olarak faturaya eklenir.</li>
                <li>Ödeme türü seçilir (Nakit, Kart, Online vb.).</li>
                <li>"Fatura Oluştur" butonuna tıklanır.</li>
            </ol>
            
            <h3>Fatura Bilgileri</h3>
            <ul>
                <li>Fatura No</li>
                <li>Müşteri Adı</li>
                <li>Alınan Hizmet(ler)</li>
                <li>Hizmet Tutarı</li>
                <li>Uygulayan Personel</li>
                <li>Tarih ve Saat</li>
                <li>Toplam Tutar</li>
                <li>Ödeme Türü (Nakit, Kredi Kartı, Online vb.)</li>
            </ul>
            
            <h3>Fatura Önizleme ve Yazdırma</h3>
            <p>"Fatura Görüntüle" veya "PDF olarak indir" seçenekleri ile çıktı alınabilir.</p>
            
            <h3>Fatura Geçmişi</h3>
            <ul>
                <li>Her müşteri için geçmişteki tüm faturalara sistemden ulaşılabilir.</li>
                <li>Tarih, hizmet, personel bazlı filtreleme yapılabilir.</li>
            </ul>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_7.png" alt="Fatura 1">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_8.png" alt="Fatura 2">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_9.png" alt="Fatura 3">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_10.png" alt="Fatura 4">
            </div>
        </div>

        <div class="section" id="kasa-hareketleri">
            <h2>💰 Kasa Hareketleri</h2>
            
            <p>Kasa modülü, işletmenizin günlük mali işlemlerini yönetmek, takip etmek ve raporlamak için kullanılır. Gelir ve giderlerin detaylı bir şekilde görüntülenebildiği bu ekran sayesinde finansal şeffaflık ve kontrol sağlanır.</p>
            
            <h3>Kasa Listesinde Görüntülenen Bilgiler</h3>
            <ul>
                <li><strong>İşlem Tarihi:</strong> Gelir veya giderin sisteme işlendiği tarih ve saat.</li>
                <li><strong>Açıklama:</strong> İşlemin nedeni (örneğin "Hizmet Ödemesi", "Ürün Satışı", "Kira Gideri").</li>
                <li><strong>Tutar:</strong> İşlemde alınan ya da ödenen miktar.</li>
                <li><strong>İşlem Türü:</strong> Gelir veya Gider olarak işaretlenir.</li>
                <li><strong>Ödeme Türü:</strong> Nakit, kredi kartı, havale, vs.</li>
                <li><strong>İşlemi Yapan Kullanıcı:</strong> Hangi personelin işlemi kaydettiği.</li>
                <li><strong>Kategori (isteğe bağlı):</strong> İşlem "Hizmet", "Ürün Satışı", "Personel Maaşı" gibi sınıflandırmalara ayrılabilir.</li>
            </ul>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_11.png" alt="Kasa Hareketleri">
            </div>
        </div>

        <div class="section" id="stok-takibi">
            <h2>📦 Stok Takibi</h2>
            
            <p>Stoklar modülü, salonunuzda kullandığınız veya satışa sunduğunuz ürünlerin giriş-çıkışlarını ve miktarlarını takip etmenizi sağlar. Envanterin düzenli takibi sayesinde eksik ürünler zamanında tespit edilir ve maliyet kontrolü sağlanır.</p>
            
            <div class="warning">
                <p><strong class="emoji">⚠️</strong> <strong>Not:</strong> Stok miktarı güncelleme, doğru stok seviyelerinin korunması için kritik bir işlemdir. Fiziksel sayımlar ve sistemdeki verilerin karşılaştırılması yoluyla yapılır.</p>
            </div>
            
            <h3>Ürün Ekleme</h3>
            <p>Yeni bir ürün sisteme eklenirken aşağıdaki bilgiler girilmelidir:</p>
            <ul>
                <li><strong>Stok Adı:</strong> Ürünün adı</li>
                <li><strong>Marka:</strong> Üretici ya da tedarikçi marka adı</li>
                <li><strong>Stok Miktarı:</strong> Başlangıçta elde bulunan miktar</li>
                <li><strong>Satış Fiyatı:</strong> Eğer satışa sunuluyorsa, müşteriye sunulan fiyat</li>
                <li><strong>Birim:</strong> Adet</li>
            </ul>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_12.png" alt="Stok Takibi">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_6.png" alt="Yeni Stok Kaydı">
            </div>
            
            <h3>Stok Miktarı Güncelleme</h3>
            <p>Kullanım ya da satış sonrası sistem, stok miktarını otomatik düşürür. Ancak istenirse elle müdahale yapılabilir:</p>
            <ul>
                <li>"Stok Güncelle" butonu ile ürün için elle giriş veya çıkış işlemi yapılır.</li>
                <li>Giriş ya da çıkış tipi belirtilir.</li>
            </ul>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_13.png" alt="Stok Güncelleme">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_7.png" alt="Stok Güncelleme Yeni Kayıt">
            </div>
            
            <h3>Filtreleme ve Arama</h3>
            <p class="note">✅ <strong>Ürünlerinizi Kolayca Bulun!</strong></p>
            <ul>
                <li>Ürün adına göre arama yapılabilir.</li>
                <li>"Stok miktarı azalan" gibi kriterlere göre sıralama yapılabilir.</li>
            </ul>
            
            <p>"Stok Yönetimini Kolayca Yapın"</p>
            <p>Stoklarınızı izlemek hiç bu kadar kolay olmamıştı! Sipariş verirken, hangi ürünlerin stokta olduğunu ve hangilerinin tükenmek üzere olduğunu anlık olarak görebilir, uygun ürünleri seçebilirsiniz. Ayrıca, sipariş geçmişinizi ve stok durumunuzu hızlıca kontrol edebilirsiniz.</p>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_14.png" alt="Filtreleme ve Arama">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_8.png" alt="Yeni Stok Grup">
            </div>
        </div>

        <div class="section" id="raporlama-ve-dışa-aktarma">
            <h2>📊 Raporlama ve Dışa Aktarma</h2>
            
            <p>"İşletmenizin Performansını Kolayca İzleyin ve Paylaşın"</p>
            <p>Belirli bir tarih aralığında personellerin yaptığı satış hareketleri raporlanabilir.</p>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_15.png" alt="Raporlama ve Dışa Aktarma">
            </div>
            
            <div class="panel-grid">
                <div class="panel">
                    <div class="panel-header">Gelir Raporları</div>
                    <p>Günlük, haftalık, aylık ve yıllık olarak gelir dağılımınızı görüntüleyebilirsiniz.</p>
                </div>
                
                <div class="panel">
                    <div class="panel-header">Personel Performansı</div>
                    <p>Personellerin hizmet ve satış performanslarını karşılaştırmalı olarak analiz edin.</p>
                </div>
                
                <div class="panel">
                    <div class="panel-header">Excel'e Aktarma</div>
                    <p>Tüm raporlarınızı Excel formatında dışa aktarabilir ve kendi analizlerinizi yapabilirsiniz.</p>
                </div>
            </div>
        </div>

        <div class="section" id="ayarlar-ve-tanımlar">
            <h2>⚙️ Ayarlar ve Tanımlar</h2>
            
            <h3>Kullanıcı Tanımlama</h3>
            <p>Ad, yetki seviyesi</p>
            
            <h4>Yeni Kullanıcı Ekleme Adımları</h4>
            <ol>
                <li>"+ Yeni Kullanıcı" butonuna tıklayın.</li>
                <li>Aşağıdaki bilgileri girin:
                    <ul>
                        <li>Kullanıcı Adı</li>
                        <li>Ad Soyad</li>
                        <li>Şifre</li>
                        <li>Yetki Seviyesi (Yönetici / Personel)</li>
                    </ul>
                </li>
                <li>Yetki seviyesi belirlenerek kullanıcı sadece belirli menülere erişebilir.</li>
            </ol>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_16.png" alt="Yeni Kullanıcı">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_9.png" alt="Yeni Kullanıcı Ekleme">
            </div>
            
            <h3>Kasa Kartı Tanımlama</h3>
            <p>Kasa işlemlerinin hangi kasa üzerinden yapıldığını belirtmek için kullanılır. (Örn: ana kasa, POS cihazı, el terminali gibi.)</p>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_17.png" alt="Kasa Kartı Tanımlama">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_10.png" alt="Kasa Kartı Tanımlama 1">
            </div>
            
            <h3>Kasa Kartı Ekleme</h3>
            <ol>
                <li>"+Yeni Kasa" butonuna basın.</li>
                <li>Kasa Adı ve Açıklaması girin.</li>
                <li>Bu kasa kartları, kasa hareketleri ve raporlama ekranlarında seçilebilir hale gelir.</li>
            </ol>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_17.png" alt="Kasa Kartı Ekleme">
            </div>
            
            <h3>Ödeme Tipi Tanımlama</h3>
            <p>Ödeme alınırken sistemde görünmesini istediğiniz ödeme yöntemlerini tanımlarsınız.</p>
            
            <h4>Örnek Ödeme Tipleri</h4>
            <ul>
                <li>Nakit</li>
                <li>Kredi Kartı</li>
                <li>Havale/EFT</li>
                <li>İndirimli Satış</li>
                <li>Online Ödeme</li>
            </ul>
            
            <p>Bu ödeme tipleri:</p>
            <ul>
                <li>Randevu sonrası ödeme ekranında</li>
                <li>Kasa hareketlerinde</li>
                <li>Fatura ekranlarında kullanılır.</li>
            </ul>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_18.png" alt="Ödeme Tipi Listesi">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_11.png" alt="Ödeme Tipi Listesi 1">
            </div>
            
            <h3>Açıklama Tanımlama</h3>
            <p>Kasa giriş ve çıkışlarında sık kullanılan açıklamaların hızlı seçimi için tanımlanır.</p>
            
            <h4>Örnek Açıklamalar</h4>
            <ul>
                <li>Ürün Alımı</li>
                <li>Müşteri İadesi</li>
                <li>Gün Sonu Devri</li>
                <li>Nakit Çekimi</li>
            </ul>
            
            <p>Bu açıklamalar, kasa hareketi eklerken hızlıca seçilebilecek şekilde görünür.</p>
            
            <div class="img-container">
                <img src="selfkuafor_readme_assets/image_19.png" alt="Örnek Açıklamalar">
            </div>
            <div class="img-container">
                <img src="selfkuafor_readme_assets/eg_12.png" alt="Örnek Açıklamalar 1">
            </div>
            
            <h3>Fatura Özel Kod Tanımlama</h3>
            <p>Faturalarda gruplama, özel raporlama veya ayrıştırma yapmak istediğiniz durumlar için kullanılır. Satış temsilcisi tanımlama ekranı.</p>
            
            <div class="img-container">
                <img src="/api/placeholder/800/450" alt="Fatura Özel Kod Tanımlama">
            </div>
            <div class="img-container">
                <img src="/api/placeholder/800/450" alt="Fatura Özel Kod Tanımlama 1">
            </div>
        </div>

        <div class="section" id="iletişim">
            <h2>📞 İletişim</h2>
            
            <div class="contact-info">
                <div class="contact-item">
                    <span class="contact-icon">✉️</span>
                    <span>E-posta: <a href="mailto:info@softmedyazilim.com">info@softmedyazilim.com</a></span>
                </div>
                
                <div class="contact-item">
                    <span class="contact-icon">📱</span>
                    <span>Telefon: <a href="tel:08505325920">0850 532 5920</a></span>
                </div>
                
                <div class="contact-item">
                    <span class="contact-icon">🌐</span>
                    <span>Web: <a href="https://softmedyazilim.com/" target="_blank">https://softmedyazilim.com/</a></span>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 2rem;">
                <a href="https://softmedyazilim.com/iletisim" class="cta-button" target="_blank">Bize Ulaşın</a>
            </div>
        </div>
    </div>

    <footer>
        <div class="container">
            <p><strong>Teşekkürler!</strong></p>
            <p>© 2025 Self Kuaför - Tüm Hakları Saklıdır.</p>
        </div>
    </footer>

    <div class="scroll-top" id="scrollTop">↑</div>

    <script>
        // Scroll to top button functionality
        const scrollTopBtn = document.getElementById('scrollTop');
        
        window.addEventListener('scroll', () => {
            if (document.body.scrollTop > 300 || document.documentElement.scrollTop > 300) {
                scrollTopBtn.classList.add('visible');
            } else {
                scrollTopBtn.classList.remove('visible');
            }
        });
        
        scrollTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 20,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>