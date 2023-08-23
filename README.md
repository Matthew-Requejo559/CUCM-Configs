# CUCM-Configs
### These are some configs for CUCM after initial install. When i first set up CUCM, i had no idea it was such a beast. I thought it was just: BOOM! install, plug in the phones, slap a config for _just_ the phone, and good to go... But i was wrong. There are actually a lot of settings and configurations that need to go on before you actually configure a phone. 

### A little preface: I originally started this lab and my [CUCM Install Lab](https://github.com/Matthew-Requejo559/CUCM-install/blob/main/README.md) because at my job, there is 1 guy who is the: Phone Commander, and they don't let other people touch the phone system. Everybody says, "Oh, it can't even be that compicated, i don't know why they don't let other people do it!" OR "Why do we gotta wait for that guy to do the phones! They should let anyone do it." NO one understood, or tried to understand, but i wanted to know. So, i acquired all the things necessary to set up my own CUCM lab at home, and see just how hard it was to install, set up, and configure a working phone system.

### As it turns out, it's pretty damn complicated. It is a huge ecosystem of settings and configurations, and if i fathered my own little enterprise CUCM baby, i wouldn't want anyone messing with it either. 

### Let's carry on with this Lab. 

### First, Lets enable all the services. We will not enable DHCP yet. Log into Cisco Unified Serviceability. Go to tools > and service activation, and activate everything except DHCP for now. Click save and OK. It takes a few minutes to start services and save. 

![001](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/a97aac9a-3ea0-4fb9-b180-eb11fab35c58)
![002](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/e4609226-e003-458f-9f9f-76a8dbd12ace)
![003](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/cc409c1f-fb69-449b-8075-b9ed947f3825)
![004](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/764ebefd-706f-4a9c-88a9-7b1477309ca3)

### Now we will go back to navigation, CUCM Administration, and change some name settings to use the CUCM ip instead of the DNS name. It makes things easier and more direct. 
### First we will go to System > Server, click find, and change the CUCM name to its IP address. in my case, 192.168.1.166. Make sure to click save after the change. 

![005](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/429b8d50-63bb-4e06-9147-55dbcdd61325)
![006](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/33e7ac4c-0f96-4ea2-b941-d15068ba75a7)
![007](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/7a1a4723-d6cf-4c93-bfb0-86077c0a0500)
![008](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/a6e14068-dd48-4bd5-9ac6-83a2caa9dfc9)
![009](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/5ae80f39-678c-4b38-a0b8-4a8479bf2835)
![010](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/0d977bce-bd41-43a0-be13-fcb835531bdc)

### Next we will go to System > Enterprise parameters and change some settings there. I am going to be using Cisco 8841 phones whcih only support SIP, so i will change the Auto registration phone protocol from SCCP to SIP. We will have to click restart, and then save, but we will do that after we chaneg the rest of the DNS settings. 

![011](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/24ae33d0-099a-440c-81d8-d6e25d926923)

### After this, lets scroll down and replace the DNS name with our CUCM IP of 192.168.1.166 in the address fields of our URL parameter settings. After this we will click save, and then reset. 

![012](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/7559f046-fde7-4813-9990-520962a8fcc6)
![013](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/8a9d7f4c-d114-47bd-bf11-5de268e945f2)
![014](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/129d43d6-9036-499e-a584-0cbaf84c756a)
![015](https://github.com/Matthew-Requejo559/CUCM-Configs/assets/136190678/467b94e6-a316-4bd2-b7b6-5684654e322f)

### Next up are service parameters 
