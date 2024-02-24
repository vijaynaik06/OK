select station_name
from station 
where line = 'violet'
and station_name NOT IN (
    SELECT station_name
    FROM station
    WHERE LINE = 'RED'
)
ORDER BY station_name ASC;
