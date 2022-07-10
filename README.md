# LVGA POINT DATASET

This folder create an algorithm to scrape data from:
https://explorer.3achain.org/token/0x1cC4967fF6592E6672827809767dF82A49f7c30D

## Data

This is a example of a value in the dataset

```ts
{
	"block": "4101482", // block number
	"time": "2022-06-21 13:13:44.000000Z", // time of transaction at Lugano timezone
	"quantity": "400", // LVGA coin tranfered
	"sender": "0x3BB4294684ef91d934b7B2aD0d8Ae09812Ae188A", // sender wallet
	"reciver": "0xF96a9f4829dBA08b7ECcb79da8B4868e5D2DFFa3" // sender reciver
}
```

The entire dataset in csv format it's saved in `/src/all.csv`
Attenction! The time is in UTC

## Automatic update of the dataset

This reposity automatically update his dataset at midnight GMT+2, the updated data is stored into the **dataset branch**. \
To get the data make an api call to the row github file, for example:

```
https://raw.githubusercontent.com/LuganoStats/LVGAPoint-Dataset/dataset/last/3month.json
```

## Manually update the dataset

```
pip install -r requirements.txt
```

to install python pagkages requirements, then

```
cd src
```

to got the the current directory, then

```
python main.py
```

it automatically download the new data and update the last inside ```/data``` folder into json syntax, as well year and month.


## Disclaimer

This project can create a lot of traffic at https://explorer.3achain.org/

Be careful: _Use it wisely_
