# Spotify Listening History — Data Dictionary
This dataset captures user listening behavior (who listened, what they listened to, when, and metadata about each track).
It is useful for building recommendations, user segmentation, and basic analytics.

| Column Name        | SQL Datatype     | Description (What This Column Means)                                   | Why This Datatype Was Used (Short)                     |
|--------------------|------------------|------------------------------------------------------------------------|---------------------------------------------------------|
| User_ID            | VARCHAR(20)      | Unique ID assigned to each user (U1, U2, etc.)                        | IDs are alphanumeric, not numeric.                     |
| Age                | INT              | Age of the user                                                       | Simple whole number.                                   |
| City               | VARCHAR(100)     | User’s city (Delhi, Mumbai, etc.)                                     | City names are text and vary in length.                |
| history_id         | VARCHAR(60) PK   | Unique ID for each listening event (H1, H2, etc.)                     | Must store text + needs to be unique.                  |
| listen_timestamp   | DATETIME         | Exact date & time the song was played                                 | Stores both date and time accurately.                  |
| liked              | TINYINT          | Whether user liked the track (0 = No, 1 = Yes)                        | Boolean → stored as 0/1.                               |
| listen_duration    | INT              | Seconds user listened to the track                                    | Duration is numeric.                                   |
| track_id2          | VARCHAR(100)     | Unique Spotify Track ID                                               | Track IDs are text, not numbers.                       |
| artists            | VARCHAR(500)     | Artist(s) who performed the song                                      | Can contain multiple names → long text.                |
| album_name         | VARCHAR(500)     | Album to which the song belongs                                       | Album names may be long.                               |
| track_name         | VARCHAR(500)     | Song title                                                            | Varied lengths → text.                                 |
| popularity         | INT              | Spotify popularity score (0–100)                                      | Numeric rating.                                        |
| duration_ms        | INT              | Duration of the song (milliseconds)                                   | Numeric field.                                         |
| explicit           | TINYINT          | Whether the track is explicit (0 or 1)                                | Boolean → compact storage.                             |
| danceability       | FLOAT            | Danceability score from 0 to 1                                        | Decimal values.                                        |
| energy             | FLOAT            | Energy level score from 0 to 1                                        | Decimal values.                                        |
| key_a              | VARCHAR(50)      | Musical key of the track (C#, G, Bb)                                  | Musical keys are text.                                 |
| loudness           | FLOAT            | Track loudness in decibels                                            | Decimal measurement.                                   |
| mode_a             | VARCHAR(50)      | Musical mode (Major / Minor)                                          | Category stored as text.                               |
| speechiness        | FLOAT            | Amount of spoken words in the track                                   | Decimal scale.                                         |
| acousticness       | FLOAT            | Acoustic probability score                                             | Decimal scale.                                         |
| instrumentalness   | FLOAT            | Instrument-only likelihood                                             | Decimal scale.                                         |
| liveness           | FLOAT            | Probability track was recorded live                                   | Decimal scale.                                         |
| valence            | FLOAT            | Positivity/happiness score of the track                               | Decimal scale.                                         |
| tempo              | FLOAT            | Beats per minute (BPM)                                                | Decimal value.                                         |
| time_signature     | INT              | Musical time signature (3/4, 4/4, etc.)                               | Whole numbers only.                                    |
| track_genre        | VARCHAR(200)     | Genre classification (pop, acoustic, indie, etc.)                    | Text field; length varies.                             |

