# Sistem Mimarisi

## Teknoloji Yığını
- **Frontend:** React.js  
- **Backend:** Node.js, Express  
- **Database:** MongoDB  
- **Message Broker:** RabbitMQ

## Mikroservisler
1. **Kullanıcı Yönetimi**  
   - Yetkilendirme ve kimlik doğrulama işlemleri  
   - API: `/api/v1/users`

2. **Ürün Yönetimi**  
   - Ürün ekleme, silme ve güncelleme  
   - API: `/api/v1/products`

3. **Sipariş Yönetimi**  
   - Sipariş oluşturma ve takip işlemleri  
   - API: `/api/v1/orders`

4. **Ödeme İşlemleri**  
   - Ödeme alma ve işlemleri  
   - API: `/api/v1/payments`

5. **Raporlama**  
   - Sistem performans raporları  
   - API: `/api/v1/reports`

## İletişim Protokolleri  
- **HTTP** üzerinden RESTful API’lardan yararlanma  
- **AMQP** üzerinden RabbitMQ ile mesajlaşma  

## Dağıtık Sistemler  
- Her mikroservis kendi veritabanına sahip  
- Servisler arası iletişim, REST ve mesajlaşma protokolleri ile sağlanır.