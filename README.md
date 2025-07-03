# alx-project-0x14

## API Overview

The **MoviesDatabase API** is a comprehensive movie and TV show data API that provides access to:

- Over 9 million titles (movies, series, episodes)
- 11 million actors and crew members
- Detailed information including ratings, cast, trailers (YouTube), awards, full biographies, etc.
- Weekly updates for recent titles and daily updates for ratings and episodes
- Multiple filters and sorting options for flexible data querying

This API is ideal for applications that require rich and updated entertainment metadata.

## Version

Current Version: **v1**

## Available Endpoints

### Titles

- **GET /titles**  
  Returns an array of titles based on optional filters and sort options.

- **GET /x/titles-by-ids**  
  Returns an array of titles by a list of IMDb IDs.

- **GET /titles/{id}**  
  Returns detailed information about a title using its IMDb ID.

- **GET /titles/{id}/ratings**  
  Returns the ratings and vote count for a given title.

- **GET /titles/series/{id}**  
  Returns all episodes for a series, sorted by season and episode.

- **GET /titles/seasons/{id}**  
  Returns the number of seasons for a series.

- **GET /titles/series/{id}/{season}**  
  Returns all episodes for a specific season of a series.

- **GET /titles/episode/{id}**  
  Returns detailed info about a specific episode.

- **GET /titles/x/upcoming**  
  Returns an array of upcoming titles.

### Search

- **GET /titles/search/keyword/{keyword}**  
  Search for titles using a keyword.

- **GET /titles/search/title/{title}**  
  Search for titles using the exact or partial title.

- **GET /titles/search/akas/{aka}**  
  Search for titles using an exact aka name (case-sensitive).

### Actors

- **GET /actors**  
  Returns a list of actors with pagination support.

- **GET /actors/{id}**  
  Returns detailed information about an actor.

### Utils

- **GET /title/utils/titleType**  
  Returns a list of available title types.

- **GET /title/utils/genres**  
  Returns a list of available genres.

- **GET /title/utils/lists**  
  Returns predefined collections of titles (e.g., top-rated, most popular, etc.)

## Request and Response Format

### Request Example

```http
GET /titles/search/title/Inception?info=base_info&limit=1
# alx-project-0x14.