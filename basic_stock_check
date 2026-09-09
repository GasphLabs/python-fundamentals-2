urun_listesi = []
ayrac = '-' * 5

while True:
    menu_secim = input(
        f'\n{ayrac} MENÜ {ayrac}\n1: Ürün Ekle\n2: Ürün Stok Kontrol\n3: Menüden Ayrıl\n\n:'
    )

    if menu_secim == '1':
        urun_ismi = input('Eklemek istediğiniz ürünün ismini girin: ')
        urun_fiyati = int(input('Eklemek istediğiniz ürünün fiyatını girin: '))
        urun_adeti = int(input('Eklemek istediğiniz ürünün stoğunu giriniz: '))

        urun_listesi.append({
            'Ürün İsmi': urun_ismi,
            'Ürün Fiyatı': urun_fiyati,
            'Ürün Adeti': urun_adeti
        })

        print(f'-> {urun_ismi} ürünü başarıyla stoğa eklendi')

        # Hatalı girdilerde soruyu tekrar sorduran doğrulama döngüsü
        while True:
            devam_mi = input('Devam etmek istiyor musunuz? (Evet/Hayır): ').lower()
            
            if devam_mi == 'evet':
                break
            elif devam_mi == 'hayır':
                print('Ana menüye dönülüyor...')
                break
            else:
                print('Hatalı giriş yaptınız! Lütfen "Evet" veya "Hayır" yazın.')

    elif menu_secim == '2':
        if not urun_listesi:
            print('Stokta henüz ürün bulunmamaktadır!\n')
        else:
            # Tüm ürünleri listeleyip arama kısmına geçiş
            for urun in urun_listesi:
                print(f'Ürün: {urun["Ürün İsmi"]} | Fiyat: {urun["Ürün Fiyatı"]} TL | Stok: {urun["Ürün Adeti"]}')
            
            aranan = input('\nAramak istediğiniz ürünün ismini girin: ')
            bulundu = False
            
            for urunler in urun_listesi:
                if aranan == urunler['Ürün İsmi']:
                    print(f'-> Aradığınız ürünün stok sayısı: {urunler["Ürün Adeti"]}')
                    bulundu = True
                    break
            
            if not bulundu:
                print('Aradığınız ürün stokta bulunamadı!')

    elif menu_secim == '3':
        print('Programdan ayrılınıyor...')
        break

    else:
        print('Hatalı tuşlama yaptınız!')
