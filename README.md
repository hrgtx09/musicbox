# MusicBox - Steps

## 1. Computer par test (optional)
1. Node.js (v18+) install karo.
2. Is folder me terminal kholo: `npm install` phir `npm start`
3. Browser me http://localhost:3000 kholo.
4. Owner login: username `owner`, password `owner123` (Library tab). Ise zaroor badlo (step 3).

## 2. Online hosting (Render.com)
1. github.com par naya repository banao aur is folder ki saari files upload karo.
2. render.com par account banao -> New -> Web Service -> apna GitHub repo chuno.
3. Settings: Runtime = Node, Build Command = `npm install`, Start Command = `npm start`.
4. Environment Variables jodo:
   - OWNER_USER = apna username
   - OWNER_PASS = apna strong password
   - JWT_SECRET = koi lamba random text
   - DATA_DIR = /var/data
5. IMPORTANT (songs gum na ho): Render me Disks -> Add Disk, Mount Path = `/var/data`, size 5 GB+.
   Disk paid plan me milti hai. Bina disk ke free plan me restart par upload kiye songs delete ho jate hain.
   (Railway.app me "Volume" add karke bhi yahi kar sakte ho, mount path /data aur DATA_DIR=/data.)
6. Deploy hone par aapko link milega, jaise https://musicbox.onrender.com

## 3. Android APK (website ko app banana)
Aasan raasta (no coding): https://www.webintoapp.com ya Median.co kholo ->
website URL me apna Render link daalo -> app ka naam, icon chuno -> Build -> APK download -> phone me install.
Website update karoge to app me apne aap update aa jayega.

## 4. Update kaise karein
GitHub me files badlo -> Render apne aap naya version deploy kar dega -> app me bhi naya aa jayega.
