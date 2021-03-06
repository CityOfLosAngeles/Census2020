# Stormwater Capture 

This repository contains the scripts to automate the calculation of stormwater capture in Los Angeles in near-real time. 

Stormwater capture is a critical part of LA's Sustainable City pLAn. See more about how we approach water capture in the [Stormwater Capture Master Plan](https://ladwp.com/ladwp/faces/wcnav_externalId/a-w-stormwatercapturemp;jsessionid=QFlXh2YNQNXJL1q8vzNGD1p2W29z2MJNtQkQ93GgGH0Nn97TyTjK!-884017759?_afrLoop=472962967276728&_afrWindowMode=0&_afrWindowId=null#%40%3F_afrWindowId%3Dnull%26_afrLoop%3D472962967276728%26_afrWindowMode%3D0%26_adf.ctrl-state%3D1dgqoxr5b_4)

This script scrapes water capture capacity datasets from the City's open data portal as well as rain guages from LA County. It checks every hour for new precipitation data. When it rains, it writes a new row to this dataset: [Water Capture by Method](https://data.lacity.org/A-Livable-and-Sustainable-City/Water-Capture-by-Method/xe35-4wsy/data)

**How much captured stormwater becomes water supply?**

Understanding exactly how much of the stormwater we capture becomes local water supply is challenging, because it depends on many factors. For example, the geology at the surface and between the land surface and the groundwater basin, the depth to groundwater basins, and whether those groundwater basins are used or accessible for water supply, all determine how much of captured stormwater becomes supply. This is especially true for projects distributed throughout the City’s landscape, such as green stormwater infrastructure. For larger projects situated over groundwater basins that are used for water supply, such as the spreading grounds, much of the captured water does infiltrate to become a part of LA’s water supply. Thus, for the purposes of this tool, we estimated 100% of stormwater captured at spreading grounds became supply.

To estimate the volumes of stormwater captured for the purposes of this dashboard, we included only the green stormwater infrastructure that contributes some water supply to the City as shown in this spreadsheet. For the purposes of this tool, we estimated 50% could potentially become water supply. There are many ways to define what becomes water supply, however. For example, in LADWP’s Stormwater Capture Master Plan it’s estimated that about 8% of the stormwater that enters the City is designated for water supply (64,000 AFY of 831,000 AFY).

More work needs to be done to more accurately understand how and where water hitting the land surface makes its way to groundwater basins. This is especially critical to quantify the amount of stormwater recharge into groundwater basins currently being used for water supply. In the Los Angeles area, more research needs to be done to quantify the contributions to groundwater storage annually from precipitation induced recharge and streamflow as well as from potential water available for artificial recharge.
