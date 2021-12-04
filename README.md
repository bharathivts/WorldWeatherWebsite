# Galytix Assessment

Hello Sir/Madam

We are going to build a World weather website using Angular. Our aim is to build website with two pages :
1. Landing Page :
Grid View :displaying all the countries in a grid having sorting, filtering and search functionality in grid.
Card View : displaying the countries in card format with their flags shown.
We need a toggle button to toggle between the above two views. On click of either this individual card or a particular row , we will navigate our user to display weather of Capital of that country.

2. Weather Page:
When we click on a particular Country either from Grid or Card view , user will be navigated to this page displaying current weather (Temperature, precipitation and wind
data) for its capital using the following API:
api.openweathermap.org/data/2.5/weather?q={{#capital#countryCode}}&amp;APPID={{#yourownappId}}

Design/Structure of project:
The aim is to build in simplest form . Since I wanted Country -weather App as common text in all my views, included that in my app.component.html. I used ag-grid for grid , Angular Material for tab and card creation as all of these things are available to use easily and gives smooth UI.

<img src="https://miro.medium.com/max/591/1*a7DIeq6o1-mA9B-3_lqfMw.png">

app.component.html having tab, divider and router-outlet tag specifies where exactly the view will be placed based on various routes


We will create a country-landing page having the toggle button to toggle in between grid and card view for showing list of countries [OnViewChange method is doing same]. On loading of this page itself we will fetch the list of countries[getCountries does that, we call that in ngOnInit]

<img src="https://miro.medium.com/max/664/1*ScM8Pt8HvyMKNkzl4QKI2g.png">

You can see the two routes above list and grid for two views:
these will be child component of above landing page , hence the below routes:

<img src="https://miro.medium.com/max/815/1*spKmDTqcvot6upZl-Nu4GQ.png">

Coming to the Grid view: We are using ag -grid , where countries is basically list of all countries to be shown as row, and columnDefs specifies the various column name of the grid:

<img src="https://miro.medium.com/max/489/1*-e_HsYQ9k5iBWBrV40fm9w.png">

Resulting in below View :
<img src="https://miro.medium.com/max/875/1*doQ4t6ySrigQQ0B4gWzNZw.png">

On click of row , we want to navigate user to Weather Page:
<img src="https://miro.medium.com/max/763/1*paf1syHXdwgD9A1sTr9pvg.png">

On click of toggle button from grid to list view , which is created using angular material card. below is code and corresponding view for it.

<img src="https://miro.medium.com/max/618/1*GVyRrEHLM0vQq-UAFUEJuw.png">

<img src="https://miro.medium.com/max/875/1*Ieljhq6JMRjsuWvagfzKkg.png">

On click of any tile/card or row of individual country , we want to display the details for that YOU WILL NEED TO GENERATE OWN APPID(signup at https://home.openweathermap.org/users/sign_in for appid)as the API call needs unique appid for sending out the data.

<img src="https://miro.medium.com/max/875/1*XM3RRttrKBDurWbjXZgD-A.png">

Calling the service above , we can fetch all the details of capital climate, display that in whatever format you wish . For now i have kept it simple as below.

<img src="https://miro.medium.com/max/875/1*_UU2FBF3yicHRic-azxgqw.png">

This is complete explanation of this World weather website.

By Vavilala Tulasi Sri Bharathi (181220057).


