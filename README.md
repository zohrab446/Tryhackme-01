# Tryhackme-01
first step at cybersecurity
# TryHackMe — Cybersecurity 101: Room 1 — Introduction

**Date:** October 2, 2025  
**Author:** Zohrab  

---

## 🎯 Summary
Bu oda siber güvenliğe giriş niteliğinde olup temel ağ, port ve servis keşfi mantığını anlamamı sağladı. İlk adım olarak bir hedef IP üzerinde port taraması yaptım, ardından web servislerini keşfederek flag(leri) buldum.  

---

## 🔍 Steps I Took

### 1. Nmap ile Keşif
- `nmap -sC -sV <ROOM_IP>` komutu ile hedefi taradım.  
- Açık portları (SSH 22 ve HTTP 80) buldum.  
- Servis versiyonlarını öğrendim (Apache, OpenSSH).

### 2. Web Servisi İncelemesi
- Tarayıcı ile `http://<ROOM_IP>` sayfasını açtım.  
- Sayfa kaynağını kontrol ettim.  
- `robots.txt` içinde gizli bir dizin (`/secret`) buldum.  
- Bu dizine giderek flag’i çıkardım:  
  - `THM{example_flag}`  

### 3. SSH Servisi Kontrolü
- SSH’nin çalıştığını doğruladım ama brute-force yapmadım.  
- Versiyon bilgisini kaydettim.  

---

## 📚 What I Learned
- `nmap` ile ilk keşfin neden önemli olduğunu gördüm.  
- `robots.txt` ve kaynak kod gibi basit yerleri kontrol etmenin flag bulmada kritik olduğunu öğrendim.  
- Varsayılan kullanıcı adı/parolaların denenmesinin bazen işe yarayabileceğini fark ettim.  
- Temel araçlar (nmap, curl, tarayıcı) ile çok şey yapılabileceğini anladım.  

---

## 🛠️ Tools I Used
- **nmap** → Port/servis keşfi  
- **curl** → Web isteklerini incelemek  
- **Firefox/Chrome** → Sayfa kaynağı ve dizin keşfi  
- **bash terminal**  

---

## ✅ Flags
- `THM{example_flag}`  

---

## 💡 Key Takeaways
- Basit adımlar (tarama + kaynak kontrolü) büyük sonuçlar verebilir.  
- Not tutmak çok önemli: her komutu ve çıktıyı kaydederek ilerlemek gerekiyor.  
- Bu süreç, TryHackMe üzerindeki diğer odalara hazırlanmak için güçlü bir temel oluşturdu.  

---
