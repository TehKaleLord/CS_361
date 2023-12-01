The way to request data from this microservice is by either typing into or writing to the string "true" into the service.txt text file.
After doing this, the microservice will generate a random number into the text same file (truncating everything else) for you to read. That
is the requesting and recieving process.


hangman game                          service.txt               microservice
      |                                     |                           |
      ||         getNumber()  (sends true)  |                           |
      ||--------------------------------->  ||                          |
      ||                                    ||                          |
      ||<-----------------------------------||      generates number   |
      ||            status                  || ------------------------>||  
      ||                                    ||                          ||
      ||                                    ||<-------------------------||
      ||               send number          ||        sendback number   ||
      ||<-----------------------------------||                          ||
      ||                                    ||                          ||
      ||                                    ||                          ||
      ||              closeRequest          ||                          ||
      ||----------------------------------> ||        close             ||
      |                                     ||------------------------->||
      |                                     |                           |     

