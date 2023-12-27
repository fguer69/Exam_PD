some errors found and corrected
Last and First Name: Warrior Francis Pius
Date: 22/12/2023

Brief summary description of changes: 
\-Add query STRUCTURE_DATA .
\-Added "@Column(unique=true)" to make the title field unique.
\-Replaced search by id with search by title in ClientWS.
\-Changed the format of some Syso's to match the track.
\-Corrected typos and distraction errors.

* * *
## CHANGES.
### PROJECT: WARRIORFRANCESCOPIO_Server.
#### FILE: Event.java
Line 27-40: Added "STRUCTURE_DATA" query.
Line 45: Added "@Column(unique=true)" to make the title field unique.

#### FILE: EventEJB.java
Line 74 - 79: Added implementation "findStructureData" method.

#### FILE: EventoRemote.java
Line 29: Added method implementation "findStructureData."

#### FILE: DatabasePopulator.java
Line 35-43: Added more instances of the entity to populate the dataBase.

#### FILE: CountInterceptor.java
Line 18-20: Added declaration and initialization outside the count method of the 3 counters.

#### FILE: MDB.java
Line 31: Added a variable to control the number of events;
Line 49-50: Created a Song s with the values just taken and saved in the database.
Line 53: Added a list and called the findAll method via ejb.
Line 56-60: Added a for loop for checking the structure.
Line 62-65 Added controls to throw events.
Line 71: Added Logger.

#### FILE: UpdateNotification.java.
Line 17: Changed content of Syso.

#### FILE: EventMultipleNotification.java.
Line 21-22: Added @Inject annotation and declaration of EventEJB.
Line 25: Changed content of Syso.
Line 26-29: Added declaration of a list, on which the multiple event persence check is performed for a structure .

### PROJECT: WARRIORFRANCOPIO_STDCLIENT.
#### FILE: Client.java
Line 21: Changed project name as desired by delivery and changed lookup accordingly:
from "java:global/Song/SongEJB!Song.SongEJBRemote" 
to java:global/GUERRIEROFRANCESCOPIO_EJB/EventEJB!server.EventEJBRemote."
Line 59: Changed the content of Syso.
Line 60: Changed songEJB.findStructure("structure").findData(date) to songEJB.findStructureData(structure, date).

### PROJECT: GUERRIEROFRANCESCOPIO_ClientWebService
#### FILE: GUERRIEROFRANCESCOPIO_ClientWebService.java
Line 37-41: Addition of Syso, variables and scanners to improve understanding of the operation to be performed.


