Description:
	I`ve created solution with few projects. I decide to spend on this project 4-8 hours in average, in fact it takes me 5 hours. And half an hour on this readme.txt.
	I stoped by the moment i make it stable and more or less cleaned up with some usefull functionality.
	I`ve finish it on monday (13th of feb) and spend half an hour for review today and minor improvements today (14th of feb).
	I`ve choosen .json file as a source. Into the solution you`ll find 3 main projects: SnappetChallenge.DataAccessLayer, SnappetChallenge.BusinessLogicLayer, SnappetChallenge.
	Dependencies are: DAL <- BLL <- SnappetChallenge.
	For the last one i use predefined mvc project cause i believe it saves me pretty much time. Also there was created projects for UnitTests, but i skip it cause of time limits (it will be one of the improvements points).
	IQueriable was returned DAL to imitate EF calls.
	Each layer wrapped with its own AutoFac module. 
	There are also some "todo" which i leave for now cause they are not that much important, but there you could see points for improvements.
	Extra libraries, tools and frameworks: newtonsoft.json, autofac (mvc integration), automapper, grid.mvc, chart.mvc (chart.js for mvc), a bit of bootstrap.
	3 pages was created besides i keep auth pages from default mvc application. Clean up its also one of the improvement points. You could navigate via top menu.
	1) SubmittedAnswer page with grid which shows list of submitted answers with filtering and ordering.
	2) Charts page shows 3 statistic charts: 
		- correct and incorrect answers (i suppose that correct = 1 is correct answer and there is no any undefined states, so only 0 and 1, but i`m not sure about it cause im not that familiar with the business domain). 
		- progress by subject (sum by progress property, probably here should be more complex logic, but for this project i suppose its enough).
		- correct answers by domain.
	3) Top students allowes to get users with the biggest progress sum and with the smallest one. You need to put subject there cause it looks senseless to calculate top by all subjects. 
Instructions:
	You need to open project, build it and launch fron visual studio. It uses db from app_data.
Credentials:
	test@test.com
	DIjob123!
Improvements:
	- UnitTests at least for BLL and DAL.
	- Mvc project cleanup from predefined stuff.
	- Make frontend much more pretty (probably could apply angularjs, or knockout and requireJs it depends on your favour)
	- Database project.
	- Prepare settings per environment (dev, test, acc, live etc).
	- Add paging logic to BLL in case of big amount of data.
	- minor imrovements are highlighted "todo:" from code.
	