# Discord Server Members
### A database of members in some large Discord servers

- ### [Info](#info-1)
- ### [Overview](#overview-1)
- ### [Database](#database-1)
  - ### [Format](#format-1)
  - ### [Servers in Database](#servers-in-database-1)
  - ### [Technical Overview](#technical-overview-1)
- ### [More Servers](#more-servers-1)

# Info
### Github Page: https://github.com/i0Z3R0/Discord-Server-Members
### Replit Page: https://replit.com/@0Z3R0/Discord-Server-Members

# Overview
#### This is a database of members of some large Discord servers (100k+). 
#### Members in the Database are **NOT** a complete list of every member, but rather most members. Read more in the technical overview section. 
#### Some members may have already left, and there is no way to avoid this. 

# Database

### [Github Database Folder](https://github.com/i0Z3R0/Discord-Server-Members/tree/main/Database )

## Format
#### All servers in the database are saved in the Sqlite3 DB file format, and converted to CSV for easier extraction. 
##### Columns in the database include members' ID, username, discriminator, and best rank. 
* ID: The ID of the user, usually an 18 digit number (very old accounts have 17)
* Discrim: The discriminator of the user, a 4 digit number or N/A if there was an error getting the discrim. Sometimes will show up as 0 if there was an server error while fetching members. 
* Best Rank: The highest ranking of the user on the member sidebar. 1 would mean they are the first user on the top of the sidebar. Useful if you would like to remove possible admins or mods, just sort by bestrank and delete the first few hundred rows. (That's still only 0.1% if the total count is 100k)
#### Simple way to extract columns in the CSV files: https://onlinecsvtools.com/extract-csv-columns

## Servers in Database
* Animal Crossing (Partnered, Community-run)
* Anime Soul Discord (Verified, Partnered)
* Apex Legends (Partnered, Official)
* Chill Heaven (Community) *****
* Emoji.gg (Community)
* Genshin Impact Official (Verified, Partnered, Official)
* Jet's Dream World (Community)
* MINECRAFT (Verified, Official)
* MrBeast Gaming (Verified, Official)
* Official Fortnite (Verified, Official)
* Pepe Server (Community)
* r/Overwatch (Partnered, Community-run)
* Rainbow 6 (Partnered, Official)
* Roblox (Partnered, Community-run)
* Rocket League Garage (Partnered, Community-run)
* Sound's World (Partnered, Official) ******
* Terraria (Verified, Official)
* VALORANT (Partnered, Official)

###### * Chill Heaven is very incomplete, despite having over 150k members online only 50k are fetched, indicating less than one third of members can see the main chat channel, indicating possible member botting or a very very serious permissions issue where most members can't see the main channel. I tried this in the rules channel, same result, about 50k members online. Not directly accusing this server of anything, but nothing like this happened to me in other servers...

###### ** Sound's World is very incomplete, less than 20% of users in the server are in the database, due to very very little users online. 

## Technical Overview
#### Members are fetched from the member list sidebar. This means in servers with over 1000 members, offline members are not fetched. Each list of members in servers are fetched every 15 minutes for several days. This captures as many online members as possible. Depending on how active a server's members are, anywhere from 5 - 75% of members can be fetched, according to my estimates. 

# More Servers
#### If you want me to add a specific server, open an issue. 
#### Several things to note before you open an issue
* The time taken will vary depending on the server. 
* The number of members fetched is dependent on the number of online users. 
* Please don't submit servers with under or around 5,000 members. 
* Please include an invite link to the server. 
* If these is a reason that I can't fetch members for you, I will let you know. 
* I am not obligated to do this for you, I am doing this in my own time so please be patient and respectful. 
