# Edirne Pansiyon Web Sitesi

Modern, SEO uyumlu ve mobil uyumlu pansiyon web sitesi.

## Özellikler

- **SEO Optimizasyonu**: Meta tag'ler, Open Graph, Twitter Card ve Schema.org yapılandırılmış veri
- **Mobil Uyumlu**: Responsive tasarım
- **Oda Galerisi**: Tek, çift ve üç kişilik odalar için gerçek görseller
- **İletişim Bilgileri**: Telefon, WhatsApp ve adres bilgileri
- **Logo Entegrasyonu**: Özel logo tasarımı

## Kurulum

### Docker ile Çalıştırma

1. **Docker ve Docker Compose'un kurulu olduğundan emin olun**

2. **Projeyi klonlayın veya indirin**

3. **Docker Compose ile çalıştırın:**
   ```bash
   docker-compose up --build
   ```

4. **Tarayıcınızda açın:**
   ```
   http://localhost:8000
   ```

### Manuel Kurulum

1. **Python 3.11+ yükleyin**

2. **Virtual environment oluşturun:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   # veya
   venv\Scripts\activate  # Windows
   ```

3. **Bağımlılıkları yükleyin:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Statik dosyaları toplayın:**
   ```bash
   python manage.py collectstatic
   ```

5. **Sunucuyu başlatın:**
   ```bash
   python manage.py runserver
   ```

## Yapılandırma

### Environment Variables

- `SECRET_KEY`: Django secret key (production için değiştirin)
- `DEBUG`: Debug modu (production'da False olmalı)
- `ALLOWED_HOSTS`: İzin verilen host'lar (virgülle ayrılmış)

### Production Deployment

1. **SECRET_KEY'i değiştirin**
2. **DEBUG=False yapın**
3. **ALLOWED_HOSTS'u domain'inize göre ayarlayın**
4. **HTTPS kullanın**

## Görsel Dosyaları

Görseller `static/images/` klasöründe bulunur:
- `logo.png`: Pansiyon logosu
- `tek.JPG`: Tek kişilik oda
- `cift.JPG`: Çift kişilik oda
- `uc.JPG`: Üç kişilik oda

## Teknik Detaylar

- **Framework**: Django 5.2
- **Python**: 3.11+
- **Veritabanı**: SQLite (varsayılan)
- **Statik Dosyalar**: Django staticfiles

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır.
