# All About Docker :-

## Why We Need Docker :-

- Jaise ki maan lo mai ek full-stack web Developer hu thik hai ,to common sense ki baat hogi ki mere pass ek khud ka local machine hoga hai thik hai ,aab bhai jaab machine bahut ovbious baat hogi n mai uss machine per kuch kaam krta rehta hu .

- jaise ki maan lo mere pass jo local machine hai maine uss ke andar window 11,rygen 5,mongoDb ya phir many more things jo maine apne local system per install kr liya hu thik hai .

---

- `Aab pta hai problem kaha hoti hai` jaise ki maan lo kuch month baad ek aur developer hire hua hai thik hai aur wo develope mere hi team mein hai thik ,to jo bhi maine apne local machine per install kiya tha ,to common sense ki baat hai mai usko github er push krta hi hu ,to jo developer aya new jiske mujhe kaam krna hai to mujhe btana hoga n ki mere local machine mein ye-ye hai tum isko download ya install kr lena ya phir mere github se clone kr lena.

- aab bhai kitni common sense ki baat hai jo new developer aya hoga mere team to mai usko bolunga n bhai tum bhi apne system ye saab install kr lo jisse tumko samjh mein aa jayega ki mai kiss project per au kaha per aur kya kaam kaar raha hu .

- **_Psychological fact :-_** jaab bhi hum kisi bade project per kaam wagera krte hai to `kis ko bhi pta nhi hota hai hamne kitna kuch tools wagera apne local machine mein install kiye hai`

---

## Main Problem :-🥵

- Aab bhai maan lo jo mera new buddy aya hai means ki jo mere team mein join hua hai ,to wo bhi saab kuch install karega n apne system mein to jaab wo saab kuch github se clone karega n to jitne envoirnment install kiya tha pehle developer ne thik wo saab enviornment ke version alag honge thik hai ,`aab yeha main picture start hota hai jaab new developer aya hoga kuch month baad to common sense ki baat usko bhi saab kuch basics se setup ya github se clone karna padega`

- To jaab wo saab kuch github se clone karega new developer jo bhi install karega to uske version conflict ho jayegenge jiske vajah se uska project run hi nhi karega,to ye to ek choti problem hai thik hai,aab tum sochoge ge ki ye choti problem kaise hai ....❓

- to choti problem isiliye hai ki `jo new developer hai n wo purane developer se baat krke ke jo version usne install kiya wahi same version new developer bhi install kar lega thik hai` to ye problem solve ho jayegi thik hai ,lekin pta hai ek aur problem aa jayegi yeha per...❓

- kyuki jo new developer hai wo to mac user hai aur jo purane developer hai wo to window user hai n ,so `jiske wajah se CLI to thik se work hi nhi kaar payega n`,mtlb ki window aur macbooki CLI tool aya command same to ho nhi sakti hai n

---

**_Notes :-_** Yedi hum isko Simple aur sedha Word mein bolu to `Multiple Enviornment -> Replicate nhi kaar pate hai sabse badi probelem yehi hoti hai`,aur Isi Problem ko Docker Easly solve kr deta hai

- Aur Suppose maan ker chalo saab kuch setup wagera kr liya but,`bhai jaab tum isko cloud per deploye karoge taab phir se env ko setup krna padega n` phir se issues hua to samjh rehe ho kitna problem face karna paad raha hai

---

### Docker ka Use krke basically ek Container create krte hai jiska use krke hum muliple enviornment ko bahut easly ek hi mein rakh sekte hai :-

- Pta hai jaab bhi hum docker ki baat krte hai n to firstly hum `ek tool use krte hai` jisko hum bolte hai **Deamon** aab pta hai ye kya hota ,iska hi use krke hum easly poora kaam ko kr lete hai ,jaise ki maan lo humko kisi kaam ko scale krna hai thik hai to specially isiliye hum use krte hai ,aur pta hai jitn abhi kaam hota hai n `jaise ki images ko create krna ,image ko pull ya phir any type stuff hi kyu n wo saab kaam hum iska hi use krke banate hai`

- Aab jaise maan lo ki mere ko image create krna hai thik hai docker ke andar to hum iske liye ek command use krte hai

```
docker run -it ubuntu

```

- to iss command ko run krte hai to pta hai ek image download hota hai aur maje ki baat to ye hai ki yedi images nhi hai n mere local machine to wo images ko install kr dega docker mere local machine mein

- aur ye bhi case ho sakta hai maan lo jaise ki mujhe jo image download krna hai n wo pehle se hai to phir se wo usi image ko download krke ek new container create karta hai .

- Aur maan lo jaise ki mere pass image nhi hai to pta hai kaha se image downlaod krte hai [hub.docker.com](https://hub.docker.com/) to yeha images download krta hai ,basically dekha jaye to ye bhi ek tarah ka github ke jaise treat hota hai lekin github nhi hota hai

- Aab jaise pta hai [Docker hub](https://hub.docker.com/) iss website per saab public container hoti hai jisko hum easly pull kr sekte hai

## Images AND Containers :-

- To Basically jaab bhi hum Docker mein hum images ki baat krte hai to ye noramll images nhi hote hai ,`hum Docker ke terms ko isko as a Opersating Sytem bolte hai`aur pta hai isi Images ko run krne ke liye humko `Humko Container ki Need ki padti hai`

- Aab maan lo jaise ki maine bola ki images ko run krne ke liye container ke need padti hai to `ye baat kuch samjh mein nhi aayi mere ko` to pta hai kya mtlb tha iska seedha aur bahut simple sa mtlb hota hai maan lo jaise koi humko iamges ko run krana hai to pta hai hum `iske liye hu multiple container ko create kr lenge phir uske andar hi iamges ko dalte chale jayenge` aur pta hai `hum ye bhi kr sekte hai aur even hota bhi hai hum ek hi images ko multiple container ke sath add kr sekte hai aur usko easly container run kr dega`

- Aur haan Jitne bhi Container hote hai wo apas mein hi `Isolated hote hai`,mtlb ki maan lo jaise maine 1st container mein jo data dala hai wo data same nhi hoga mtlb jaab 2nd container jo data ayega wo data diffrent hoga ,yeha per `isolated ka mtlb ye hota hai`

- Isolated ka yedi hum Simple sa mtlb dekhe to Apas mein Communicate nhi kaar sekte hai

#### Here Some Docker Related Command :-

```
👀 docker run -it your image name
<!-- For Ruunig The Docker Container -->

👀 docker container ls
<!-- So The Container Will Be listed in Current Container -->

👀 docker container ls -a
<!-- So The All Container Will be Listed in Our Terminal  -->

👀 docker start your container name
<!-- Restart Your Closed Container -->

👀 docker stop your container name
<!-- Close Your Container -->

👀 docker exec your container name ls
<!-- Execute your container -->

👀 docker exec -it your name bash
<!-- Conect our terminal with Docker terminal -->

👀 docker images 
<!-- FOe See Your Images -->


👀 docker run -it -p
<!-- For run at Port Maping -->

```

- [portainer](https://docs.portainer.io/)

- Aur pta hai Mainly dekha jaye to to `most of the companies bahut smartly apne project kisi bhi machine per run kr leti hai `,sabse best yehi use hota hai docker ka ,jiske wajah se apne poore machine ko local server per run kara lete hai 

- aur pta hai iska fayeda sabse jyada taab hota hai jaab jaab koi bhi serve or project self hosted karana ho to taab.

## Port Maping :-

### What Is Exactly Port Runing :-

- Jaise ki maan lo mere pass ek container hai thik hai ,aur hum `iss container ke andar node js ko run kaar rehe hai thik hai` ,`aur bhai ye to common sense ki baat hai ki jaab ek container ke node js run kaar raha hai to ye ek serve hi hoga`

- Aur bhai taab tumko to ye bhi pta hona chaiye ki **kisi bhi type ke server ko run krne ke liye PORT:5000 hona jaruri hota hi hai** aur yaad hoga jo bhi server hai n wo saab to container ke andar hi hote hai jaise ki maine pehle hi bola hai,aur`jaise ki pta hai container to isloated hi hoti hai `  ,aab iska kya mtlb jaab tum koi aur dusri container ko open karoge aur uss container ke andar jaab tum node js ko search krte ho to wo `server not found dega because of CONTAINER IS ISOLATED` 

- Aur pta hai kyu server not found aa raha hai becasuse of jo server chal raha hai n wo uss container ke andar chal raha hai thik hai ,Aab pta hai isko access lene ke liye humko is port ko `EXPOSE` krna hoga jisese humko pta chal sake

- Aur aab Hum expose krne keliye ek method use krte hai jisko bolte hai hum `mailhog` ye ek serve hota jisko run karane ke baad hum uss port ko easly expose kaar sekte hai 

### What Is Mailhog Server :-

- To basically ye ek tarah se server hota hai ,mtlb ki iska  name hi hota hai `mailhog server` aur dekha jaye to ye ek tarah ka Images hote hai jiska use krke hum mail ko send kaar sekte hai 

- Aur `mailhog server` 

```
👉 always 1025 port per run hota hai

```

- Aur jaab bhi port maping ka use krte hai `always try krna chaiye ki hum conatiner ek andar jo server /images run krta hai uska hi name likhan chaiye`


#### For Example :-

```

docker run -it -p 1025:ecstatic_brahmagupta

```

- Note :- Sabse Important baat during the container banaye time kisi bhi type ka container ho memory ko bahut jyada cosumekrta haii 

