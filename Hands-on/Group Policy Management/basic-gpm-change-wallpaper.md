# Set Wallpaper to Users' End from Server

Server: 
File Explorer> Desktop > Create ImageHere > wallpaper.jpg > Properties > 
Sharing > Advanced Sharing > Share this folder > Share name "ImageHere$" > Permission > User {Cindy} > Check Name > Full control 
Security > Advanced > Disable Inheitance > Edit > Add Cindy > Full Control

Server Manager > Tools > Group Policy Mgmt. > 
GPM > Forest > somain {cincin.com} > Create GPO.., > Name to "Lock Wallpaper Change" > Navigate "Lock Wallpaper Change" {domain.com} and GPO > Edit > Desktop > Wallpaper > Paste Path ex: .... "ImageHere$\wallpaper.jpg"
> Enable > Apply
