Download Link: https://assignmentchef.com/product/solved-s670-problem-set-4
<br>
Download the following two files from https://datasets.imdbws.com/: title.ratings.tsv.gz and title.basics.tsv.gz. (You may need to download software to unzip the file, e.g. 7Zip.) The unzipped files are in tab separated value form. (Warning: the latter file is about half a gigabyte unzipped.)

Unzip the files and read them into R. Using read tsv or read delim is recommended, e.g.: read_tsv(“title.ratings.tsv”, na = “\N”, quote = ’’)

(Those are supposed to be straight quotes. You’ll get a few tens of thousands of warnings, but these pertain to the variable endYear, which is irrelevant for our purposes.) Merge the two data sets by the unique identifier tconst. We only want movies, so only keep data for which titleType is “movie.” After doing this, I ended up with about 240,000 movies.

<h1>Questions</h1>

<ol>

 <li>Fit a model to predict a movie’s IMDB rating (variable averageRating) by year (startYear) and length (runtimeMinutes.) You will have to make a number of modeling choices:

  <ul>

   <li>Do you need any transformations?</li>

   <li>Should you fit a linear model or something curved?</li>

   <li>Is an additive model adequate?</li>

   <li>Do you need to filter out or downweight tail values to prevent the fit from being dominated by outliers?</li>

   <li>Should you weight by number of votes?</li>

  </ul></li>

</ol>

Some of these choices are clear-cut, while others will be a matter of preference. You must justify all your choices. You’ll be graded on the justification, not the choice (unless the choice is really bad.)

Note that computational concerns will also drive your modeling choices. For example, you will not be able to put all the data into a loess unless you have a supercomputer.

1

<ol start="2">

 <li>Draw ONE set of faceted plots to display the model — either condition on year or length,whichever seems to you to be more interesting. Choose a sensible number of panels. Briefly describe what this set of plots shows you.</li>

 <li>Draw a raster-and-contour plot (or other “3D” plot of your choice) to further display yourmodel. The plot should show predictions for the majority of movie years and lengths (you don’t have to show outliers.) Briefly describe what, if anything, this plot shows you that your plot for question 2 didn’t.</li>

 <li>Answer the substantive question: Do longer movies tend to get higher IMDB ratings, afteraccounting for their year of release? (The answer will likely be more complicated than “yes” or “no.”)</li>

</ol>