Question 1:
The columns provide order info. There is order_id that shows what order items are associated with. Quantity shows how many of each item where in the order. Item name is the name of the item. Item_price shows price for the items chosen. Choice_description provides info on customer choices within the order (such as what is used in a burrito). 
Rows are items within an order. 


Code:

$ head chipotle.csv

$ tail chipotle.csv

Question 2:
1834
Code:

$ wc chipotle.csv

Question 3:

There are 4,623 lines in the file.

Code:

$ wc chipotle.csv

Question 4:

The chicken burrito is in 553 orders while the steak burrito is in 368.
Code:

$ grep "Steak Burrito" chipotle.csv | wc

$ grep "Chicken Burrito" chipotle.csv | wc

Question 5:
Black beans are in 282 burritos, while pinto are in 105
Code:
$ grep "Chicken Burrito" chipotle.csv | grep -i "black beans" | wc

$ grep "Chicken Burrito" chipotle.csv | grep -i "pinto beans" | wc


Question 6:

There are 24 *.csv and *.tsv files in the DAT2 repo:

find . -name *.?sv
./data/airlines.csv
./data/Airline_on_time_west_coast.csv
./data/bank-additional.csv
./data/bikeshare.csv
./data/chipotle.tsv
./data/citibike_feb2014.csv
./data/drinks.csv
./data/drones.csv
./data/hitters.csv
./data/icecream.csv
./data/imdb_1000.csv
./data/mtcars.csv
./data/NBA_players_2015.csv
./data/ozone.csv
./data/pronto_cycle_share/2015_station_data.csv
./data/pronto_cycle_share/2015_trip_data.csv
./data/pronto_cycle_share/2015_weather_data.csv
./data/sms.tsv
./data/syria.csv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.csv Code Used:

$ find . -name *.?sv

Question 7:

81 times
Code:

$ grep -ir dictionary . | wc

Question 8: (Optional)

26 [Coca Cola]
     18 [Dr. Pepper]
     17 [Sprite]
     15 [Mountain Dew]
     15 [Diet Coke]
     13 [Diet Dr. Pepper]
Code:
$ grep -i "canned soda" chipotle.csv | cut -f4 | sort | uniq -c | sort -r
