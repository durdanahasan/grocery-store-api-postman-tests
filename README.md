# 🛒 Simple Grocery Store API - Postman Test

Bu Postman kolleksiyası **Simple Grocery Store API**-nin (`https://simple-grocery-store-api.click`) avtomatlaşdırılmış test edilməsi və əsas funksionallıqlarının yoxlanılması üçün hazırlanmışdır.

---

## 🚀 Xüsusiyyətlər və Endpoint-lər

Kolleksiya aşağıdakı əsas modulları əhatə edir:

1. **Auth (Autentifikasiya):** 
   - Yeni APIclient qeydiyyatı (`POST /api-clients`) və əldə olunan `accessToken`-in avtomatik olaraq environment dəyişəni kimi yadda saxlanılması.
2. **Status:** 
   - API-nin işlək vəziyyətdə olmasının yoxlanılması (`GET /status`).
3. **Products (Məhsullar):** 
   - Bütün məhsulların siyahısının alınması (`GET /products`).
   - ID-yə görə spesifik məhsulun tapılması (`GET /products/:productId`).
   - Səhv ID ilə neqativ testlərin aparılması.
4. **Cart (Səbət əməliyyatları):** 
   - Yeni səbət yaratmaq (`POST /carts`).
   - Səbətə məhsul əlavə etmək (`POST /carts/:cartId/items`).
   - Səbət məhsullarını oxumaq, miqdarı yeniləmək (`PATCH`) və silmək (`DELETE`).
5. **Sifarişlər (Orders):** 
   - Səbət vasitəsilə sifariş yaratmaq, sifarişləri siyahılamaq, təkrar yoxlamaq və yeniləmək.
   - Avtorizasiya olunmamış sorğular üçün neqativ testlər (`401 Unauthorized`).

---

## 🛠️ Necə İstifadə Etməli?

1. **Postman-də açın:** 
   - `E-CommercePostman.json` faylını Postman tətbiqinə sürükləyib buraxın (`Import` edin).
2. **Environment qurun:** 
   - Kolleksiya daxilində `baseUrl` dəyişəni yaradın və dəyərini `https://simple-grocery-store-api.click` olaraq təyin edin.
3. **Testləri işə salın:** 
   - Əvvəlcə **Auth -> Register API client** sorğusunu göndərin (token avtomatik olaraq yadda saxlanılacaq), daha sonra digər sorğuları ardıcıl şəkildə test edin.
