08/04: Initialization of the project

09/04: Backend configuration and frontend initialization

10/04: Basic frontend with React (learning how to make it work)

11/04: Basic frontend with React (learning how to make it work)

12/04: Worked authentication and sessions, and change of structure in frontend instead of using React will be SSR

15/04: Add template system using Templ and optimized session system

16/04: Add session system to validate authentication and user authorization

17/04: Fixed session system, and started the administrator panel. Added basic styles of
admin panel. Added automated "tasks" configuration (npm run build, npm run watch, etc.)

18/04: Add functionality to change the base path of the site (e.g. example.com/rutabase/). Added styles for the administrator panel and Basque modal functionality.
![](images/Pasted%20image%2020240418195931.png)

19/04: Updated model to correctly store library information in the database

22/04: Revert the use of a modal for the form to a page of its own.
![](images/Pasted%20image%2020240423001958.png)
![](images/Pasted%20image%2020240423002008.png)

23/04: Add base to be able to read disk files. Installed package to interact with TMDB api.

24/04: Add functionality to list movies from a library. Search for your metadata and save them in the database. Started home page with navbar and sidebar.
![](images/Pasted%20image%2020240424202934.png)
![](images/Pasted%20image%2020240424203001.png)

25/04: Add sidebar and navbar for normal users. Styles have been modified to accommodate previous styles with new ones.
![](images/Pasted%20image%2020240425200716.png)
![](images/Pasted%20image%2020240425200726.png)
![](images/Pasted%20image%2020240425200748.png)

28/04: Remodeling the data structure to be able to host different types of files in a single type of data. In this way we can have Movies, Series, Timings and Chapters in a single table and as a single entity. A library view has also been added, using a JS pack to add reactivity to the design and make it responsive in case of opening the sidebar:
![](images/Pasted%20image%2020240428043800.png)
![](images/Pasted%20image%2020240428044619.png)
![](images/Pasted%20image%2020240429155309.png)
![](images/Pasted%20image%2020240429151515.png)

29/04: Small fixes errors.

30/04: Add functionality to index items, whether films, series, seasons or chapters.
![](images/Pasted%20image%2020240430203537.png)

01/05: Added functionality to search for metadata from items indexed in the database, whether films or series, and provided the basis to later add seasons and chapters.

![](images/Pasted%20image%2020240502074558.png)

02/05: Add functionality to search for metadata using identifiers from other metadata providers. For example, files with IMDB identifiers, search them in TMDB. The interface has also been fixed to accommodate size and scroll changes (previously it was malfunctioning)

![](images/Pasted%20image%2020240503062945.png)

03/05: Modified model to add credits to a film, and people to credits:

![](images/Pasted%20image%2020240504022728.png)
![](images/Pasted%20image%2020240504022958.png)

06/05: Add code to request movie credits and add a list of directors, writers and actors to the view:

![](images/Pasted%20image%2020240508050522.png)
![](images/Pasted%20image%2020240508050542.png)

(The director is not seen in the image, because it is missing to implement that a person can have more than one credit in a film, since he can be an actor and also director, writer, etc. In this case, the director is an actor, Jon Favreau)

07/05: Added indexing of season and chapter metadata.

08/05: Add seasons of a series to the series page. Modified the item model to be able to add an end date in case of being a series.
![](images/Pasted%20image%2020240508155030.png)

09/05: Added extra metadata for items:
- Series have as their final date the last chapter that has been issued.
- All items that have external metadata, have the note (external)
- Added the duration of an item. In case of being a container (series or season) it contains the sum of the children
- Using the duration, a calculation of when it ends in case of starting the playback at the time has been added.

![](images/Pasted%20image%2020240510060037.png)
![](images/Pasted%20image%2020240510060213.png)

10/05: Fixed responsibility for the item details page.

Before:
![](images/Pasted%20image%2020240510172910.png)
Then:
![](images/Pasted%20image%2020240510172934.png)

13/05: Add play button, and basic element playback feature.
![](images/Pasted%20image%2020240513202403.png)
![](images/Pasted%20image%2020240513233319.png)

14/05: Modified player to add functionality with keyboard and show the finish time.
![](images/Pasted%20image%2020240515184621.png)

15/05: Modified model to store "devices". In this way we can differentiate between "devices" of the same user, and in case of using "Sync", we can identify whether it is the device that has been pointed to the sync or not.

16/05: Modified the "device" model to allow the storage of an API key to be identified when making requests without cookies, as is the case with WebSockets.

20/05: Add functionality to create, join and exit sync groups.
![](images/Pasted%20image%2020240521052524.png)
![](images/Pasted%20image%2020240521052536.png)
![](images/Pasted%20image%2020240521052659.png)

22/05: Added basic playback synchronization functionality. Supports synchronization between any number of users (as many as the server supports). Any user can join a room that is playing a video and will automatically sync. The option to play new content in an existing session has also been added (while someone is playing content.)
![](images/Pasted%20image%2020240522161251.png)
![](images/Pasted%20image%2020240522161305.png)

24/05: Added context of "buffer" when doing Syncplay. Now if a user has a slower connection and its reproduction is paused, the other users are informed that a user is waiting, so they will also wait.

25-26/05: Modified styles and design, such as the colors of the main theme, the source, noise effect and scanlines, etc.
Added to start-up a card of your own for each library, also added to start-up, the latest latest items in each library.
![](images/Pasted%20image%2020240527173659.png)
In the library part, an option has been added to sort content
![](images/Pasted%20image%2020240527174015.png)

27/05: The "Persona" page has been added, with personal information and credits on the website.
![](images/Pasted%20image%2020240528183358.png)

28/05: Work on the final document begins.

29/05: Performed deployment using Docker in demo1.ovo.watch address

30/05: Fixed bugs related to SQLite.