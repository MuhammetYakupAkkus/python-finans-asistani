# python-finans-asistani
Para çekip yatırabileceğin ufak bir banka platformu
bakiye = 1000.0
while True:
    
    giriş = int(input("\n--BÜTÇE TAKİP PROGRAMI--\n1.Bakiyeyi Görüntüle\n2.Para Yatır(Gelir Ekle)\n3.Para Çek\n4.Bakiyeyi Doğrudan Değiştir\n5.Çıkış\nYapmak İstediğiniz Seçeneğin Numarasını Yazın:" ))
    if giriş == 1:
        print("\nBakiyeyi görüntüleme işlemi seçildi.")
        print("Bakiyeniz:" + str(bakiye))
        while True:
            bky = float(input("1.Ana Menüye dön\nŞimdi ne yapmak istiyorsunuz."))
            if bky == 1:
                print("Ana Menüye Dölüyor")
                break
            else:
                print("Yanlış Kodlama Yaptınız")

    elif giriş == 2:
        anamenu = False
        while True :
            print("\nPara yatırma işlemi seçildi.")
            para_yatirma = int (input("Kaç TL Yatıracaksınız:"))
            bakiye += para_yatirma
            print("Güncel Bakiyeniz:" + str(bakiye))
            while True:
                bky = float(input("1.Yeniden Para Yatır\n2.Ana Menüye dön\nŞimdi ne yapmak istiyorsunuz."))
                if bky == 1:
                    print("Yeniden Para Yatırılıyor")
                    break
                        
                elif bky ==2 :
                    print("Ana Menüye Dönülüyor")
                    anamenu = True
                    break

                else:
                    print("Yanlış Kodlama Yaptınız")
            if anamenu :
               break

    elif giriş == 3:
        anamenu : False
        while True:
            anamenu : False
            print("\nPara çekme işlemi seçildi.")
            print("Bakiyeniz:"+str(bakiye))
            while True:

                para_çekme = int (input("Kaç TL Çekmek İstiyorsunuz:"))
                if bakiye < para_çekme:
                    print("Yetersiz Bakiye")
                    bky = float(input("Paranız Çekilememiştir.\n1.Yeniden Para Çek\n2.Ana Menüye dön\nŞimdi Ne yapmak İstiyorsunuz:"))
                    if bky==1:
                        print("Yeniden Para Çekiliyor")
                    elif bky == 2:
                        print("Ana Menüye Dönülüyor")
                        anamenu = True
                        break
                    else:
                                            print("Yanlış Kodlama Yaptınız")
                else :
                    bakiye -= para_çekme
                    print(f"\nGüncel bakiyeniz: {bakiye} TL")
                    bky = float(input("Paranız Çekilmiştir.\n1.Yeniden Para Çek\n2.Ana Menüye dön\nŞimdi Ne yapmak İstiyorsunuz:"))
                    if bky==1:
                        print("Yeniden Para Çekiliyor")
                        anamenu : False
                        
                    elif bky == 2:
                        print("Ana Menüye Dönülüyor")
                        anamenu = True
                        break
                    else:
                        print("Yanlış Kodlama Yaptınız")
            if anamenu:
                break
        if anamenu:
             continue
    elif giriş == 4:
        anamenu = False
        print("\nPara Düzenleme Ekranı Seçildi")

        while True:
            yeni_bakiye = float(input("Yeni bakiye miktarını girin: "))

            if yeni_bakiye < 0:
                print("Hata: Bakiye 0'dan küçük olamaz!")
                continue
            else:
                bakiye = yeni_bakiye
                print(f"Güncel bakiyeniz: {bakiye} TL")

            while True:
                alt_secim = int(
                input("1. Bakiyeyi Tekrar Düzenle\n2. Ana Menüye Dön\nSeçiminiz: "))

                if alt_secim == 1:
                    anamenu = False
                    break
                elif alt_secim == 2:
                    print("Ana Menüye Dönülüyor...")
                    anamenu = True
                    break
                else:
                    print("Yanlış Kodlama Yaptınız!")

            if anamenu:
                break

        if anamenu:
            continue

    elif giriş == 5:
        print("Çıkış Yapılıyor...")
        break


     
