# donorschoose-recommender

Out-of-competition dabbling with DonorsChoose.org data from [Kaggle](https://www.kaggle.com/donorschoose)

## Installation of this project
```
$ cd
~$ mkdir work
~/work$ git clone https://github.com/fdurant/donorschoose-recommender.git
~/work$ cd donorschoose-recommender
~/work/donorschoose-recommender$ 
```

## Setup

```
~/work/donorschoose-recommender$ mkdir data
~/work/donorschoose-recommender$ cd data
~/work/donorschoose-recommender/data$
```

Go to the DonorsChoose.org Kaggle page and download the data into this 'data' directory.
The result should look like this:
```
~/work/donorschoose-recommender$ ls -1 data
Donations.csv
Donors.csv
Projects.csv
Resources.csv
Schools.csv
Teachers.csv
~/work/donorschoose-recommender$
```

Optionally, compress the data on your local disk
```
~/work/donorschoose-recommender$ cd data
~/work/donorschoose-recommender/data$ for FILE in *; do gzip $FILE; done
~/work/donorschoose-recommender/data$ ls -1
Donations.csv.gz
Donors.csv.gz
Projects.csv.gz
Resources.csv.gz
Schools.csv.gz
Teachers.csv.gz
```

## Prepare environment file for Docker
```
~/work/donorschoose-recommender/data$ cd ..
~/work/donorschoose-recommender$ cat > .env
DATADIR=/&lt;yourhomedir&gt;/work/donorschoose-recommender/data
NOTEBOOKSDIR=/&lt;yourhomedir&gt;/work/donorschoose-recommender/notebooks
(Ctrl-D)
```
where &lt;yourhomedir&gt; is replaced with the full path to your actual home directory.

## Launch the notebook
```
$ docker-compose up -d --build anaconda3
```

Go to [http://localhost:8888](http://localhost:8888)


## Stop the notebook
```
$ docker-compose stop anaconda3
```
