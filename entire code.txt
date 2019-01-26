(defrule compare-object
=>
(printout t "What do you want to compare (car or byke)?")
(assert (object-to-compare (read))))


(defrule cc-of-byke
(object-to-compare byke)
=>
(printout t "are you looking for a byke greater than 125cc (yes or no)?")
(assert (byke-of-cc (read))))


(defrule mileage-of-byke
(and (object-to-compare byke)
(byke-of-cc yes))
=>
(printout t "what kind of mileage are you expecting for your byke(high or low)?")
(assert (byke-of-mileage (read))))


(defrule looks-of-byke
(object-to-compare byke)
=>
(printout t "do you want a byke wich looks ultra modern (yes or no)?")
(assert (byke-of-looks (read))))



(defrule price-of-byke
(object-to-compare byke)
=>
(printout t "you are comfortable with a byke of prize (high or low)?")
(assert (byke-of-price (read))))


(defrule related-byke1
(and (byke-of-cc no)
(byke-of-looks yes)
(byke-of-price low))
=>
(printout t "T.V.S SPORT or HERO HONDA SPLENDOR "))


(defrule related-byke2
(and (byke-of-cc no)
(byke-of-looks yes)
(byke-of-price high))
=>
(printout t "T.V.S CITY or HONDA TWISTER "))



(defrule related-byke3
(and (byke-of-cc no)
(byke-of-looks no)
(byke-of-price low))
=>
(printout t "T.V.S HEAVY DUTY"))


(defrule related-byke4
(and (byke-of-cc no)
(byke-of-looks no)
(byke-of-price high))
=>
(printout t "CONSULT AGAIN"))


(defrule related-byke5
(and (byke-of-cc yes)
(byke-of-mileage high)
(byke-of-looks yes)
(byke-of-price high))
=>
(printout t "HONDA SHINE"))


(defrule related-byke6
(and (byke-of-cc yes)
(byke-of-mileage high)
(byke-of-looks yes)
(byke-of-price low))
=>
(printout t "HERO HONDA PASSION"))


(defrule related-byke7
(and (byke-of-cc yes)
(byke-of-mileage low)
(byke-of-looks yes)
(byke-of-price low))
=>
(printout t "BAJAJ PULSAR"))


(defrule related-byke8
(and (byke-of-cc yes)
(byke-of-mileage low)
(or(byke-of-looks low)
(byke-of-price high)))
=>
(printout t "YAMAHA R15"))


(defrule type-of-car
(object-to-compare car)
=>
(printout t "what kind of a car are you looking for (petrol or diesel)?")
(assert (car-of-type (read))))


(defrule capasity-of-car1
(and (object-to-compare car)
(car-of-type petrol))
=>
(printout t "do you want a car greater than seating capacity 4(yes or no)?")
(assert (car-of-capacity1 (read))))


(defrule looks-of-car1
(and (object-to-compare car)
(car-of-type petrol))
=>
(printout t "do you want a car wich looks ultra modern (yes or no)?")
(assert (car-of-looks1 (read))))


(defrule price-of-car1
(and (object-to-compare car)
(car-of-type petrol))
=>
(printout t "you are comfortable with a car of prize (high or low)?")
(assert (car-of-price1 (read))))


(defrule related-car1
(and (or (car-of-type petrol)
(car-of-looks1 yes))
(car-of-capacity1 yes)
(car-of-price1 high))
=>
(printout t "GO FOR SCORPIO!! "))


(defrule related-car2
(and (or (car-of-type petrol)
(car-of-looks1 yes))
(car-of-capacity1 no)
(car-of-price1 high))
=>
(printout t "GO FOR SWIFT!! "))


(defrule related-car3
(and (or (car-of-type petrol)
(car-of-looks1 yes))
(car-of-capacity1 yes)
(car-of-price1 low))
=>
(printout t "GO FOR MARUTHI VAN!! "))


(defrule related-car2
(and (or (car-of-type petrol)
(car-of-looks1 yes))
(car-of-capacity1 no)
(car-of-price1 low))
=>
(printout t "GO FOR I 10!! "))


(defrule capasity-of-car2
(and (object-to-compare car)
(car-of-type diesel))
=>
(printout t "do you want a car greater than seating capacity 4(yes or no)?")
(assert (car-of-capacity2 (read))))


(defrule looks-of-car2
(and (object-to-compare car)
(car-of-type diesel))
=>
(printout t "do you want a car wich looks ultra modern (yes or no)?")
(assert (car-of-looks2 (read))))


(defrule price-of-car2
(and (object-to-compare car)
(car-of-type diesel ))
=>
(printout t "you are comfortable with a car of prize (high or low)?")
(assert (car-of-price2 (read))))


(defrule related-car5
(and (or (car-of-type diesel)
(car-of-looks2 yes))
(car-of-capacity2 yes)
(car-of-price2 high))
=>
(printout t "GO FOR SCORPIO!! "))


(defrule related-car6
(and (or (car-of-type diesel)
(car-of-looks2 yes))
(car-of-capacity2 no)
(car-of-price2 high))
=>
(printout t "GO FOR SWIFT!! "))


(defrule related-car7
(and (or (car-of-type diesel)
(car-of-looks2 yes))
(car-of-capacity2 yes)
(car-of-price2 low))
=>
(printout t "GO FOR MARUTHI VAN!! "))


(defrule related-car8
(and (or (car-of-type diesel)
(car-of-looks2 yes))
(car-of-capacity2 no)
(car-of-price2 low))
=>
(printout t "GO FOR I 10!! "))
