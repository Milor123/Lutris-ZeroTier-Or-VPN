# Connect a wine game with VPN Tunnel in linux

For this example we use the new Baldurs Gate III for play via online LAN using a VPN for play with friends like local network

## Requeriments:

- Install VPN over you linux network, for my case I've used ZeroTier One, (install configure and test that it work nice in your linux).
- Install Bottles or Lutris or you wine manager preferred (for this example I'll use lutris)
- Install your game
- Install IPXwrapper (Download an extract file over your game main folder, where is the main .exe file, not the launcher, the main file, for the case of baldurs gate we search the **folder** where is the files **bg3.exe or bg3_dx11.exe** )

After of have all in order and stay sure that VPN works nice over linux, now we need hook it in windows, in the wine.

Need execute the `ipxconfig.exe` the which was extracted before (IPXwrapper), execute this file using ==**Run EXE inside wine prefix**== or whatever that allow execute this file in the wine (bottles, lutris, etc)

![image](https://github.com/Milor123/Lutris-ZeroTier-Or-VPN/assets/14153649/d5f47b96-f240-44f1-9063-5e1745a175d7)

## Wine config:

Next in the Wine configuration, under Libraries tab add **wsock32** in New override for library, and set it to use Native then Builtin under Edit Override

![ConfigureWineVPN-1](https://github.com/Milor123/Lutris-ZeroTier-Or-VPN/assets/14153649/0f088875-e652-41eb-9a35-d3fac3bcec35)

![ConfigureWineVPN-2](https://github.com/Milor123/Lutris-ZeroTier-Or-VPN/assets/14153649/0b39af83-37e8-4b2b-ad14-7ab2be9d33ad)

Also you probably could add it in **DLL override options** of your wine manager or using **enviroment variables**.

![DLL-Override-Lutris](https://github.com/Milor123/Lutris-ZeroTier-Or-VPN/assets/14153649/b82206c6-542c-42cb-9ae9-2b620b9937a8)
