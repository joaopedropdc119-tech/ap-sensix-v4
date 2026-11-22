# AP SENSIX V4.0 — projeto Android

Este pacote contém o aplicativo web e a configuração Capacitor para empacotar como APK Android.

## Como gerar o APK com GitHub Actions (sem instalar Android Studio no celular)
1. Crie um repositório no GitHub e envie todos os arquivos desta pasta.
2. No GitHub, abra **Actions** e permita executar workflows.
3. O workflow `Build Android APK` compila o APK de depuração.
4. Baixe o artefato `AP-SENSIX-debug-apk` ao final da execução.
5. Instale o APK no Android. Talvez seja necessário permitir instalação desta fonte.

## Gerar localmente (PC com Node.js e Android SDK)
```bash
npm install
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```
O APK ficará em `android/app/build/outputs/apk/debug/app-debug.apk`.

## Limitações atuais
- A conta é apenas um nome local, não existe login em servidor.
- Perfis ficam no armazenamento local do aparelho; não sincronizam.
- Não modifica o Free Fire e não oferece aimbot, mira automática ou cheats.
- Este projeto gera um APK Android de teste/debug. Publicação na Play Store exige configuração de assinatura e políticas da loja.
