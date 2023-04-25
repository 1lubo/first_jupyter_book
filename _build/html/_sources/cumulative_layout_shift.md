
# Cumulative layout shift (CLS)

CLS is a measure of the largest burst of layout shift scores for every unexpected layout shift that occurs during the entire lifespan of a page.

A layout shift occurs any time a visible element changes its position from one rendered frame to the next. (See below for details on how individual layout shift scores are calculated.)

A burst of layout shifts, known as a session window, is when one or more individual layout shifts occur in rapid succession with less than 1-second in between each shift and a maximum of 5 seconds for the total window duration.

The largest burst is the session window with the maximum cumulative score of all layout shifts within that window.


![figure](cumulative_layout_shift.png)