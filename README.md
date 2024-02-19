# Instagram-database-clone
This Instagram Database Clone is designed to replicate the functionality of the popular social media platform Instagram. It includes several interconnected tables within a MySQL database to efficiently store user information, posts, comments, likes, follows, and other relevant data.

## Features
- Users: Store user account information such as username, id and timestamps.
- Photos: Save id, image_url, user_oid and Timestamps.
- Comments: Allow users to comment on posts with text and timestamps.
- Likes: Enable users to like posts with timestamps.
- Follows: Track user connections by storing follower and following relationships.
- Tags and Photos Tags: Implement tagging functionality to categorize posts.

## Tables
### Users Table:
- Fields: id, username, created_at

### Photos Table:
- Fields: id, image_url, user_id (foreign key referencing Users table), created_at

### Comments Table:
- Fields: id, photo_id (foreign key referencing Photos table), user_id (foreign key referencing Users table), comment_text, timestamp.

### Likes Table:
- Fields: photo_id (foreign key referencing Photo table), user_id (foreign key referencing Users table), timestamp.

### Follows Table:
- Fields: followee_id (foreign key referencing Users table), follower_id (foreign key referencing Users table), following_id (foreign key referencing Users table), timestamp.

### Tags Table:
- Fields: id, tag_name, timestamp.

### Photo Tags Table:
- Fields: photo_id (foreign key referencing Photos table), tag_id (foreign key referencing Tags table).

## How to Use
- Setup MySQL Database: Create a MySQL database and import the provided schema (SQL file) to create the necessary tables.
- Configure Connection: Update the database connection details in your application code or script to point to the newly created MySQL database.
- Implement Functionality: Develop application features such as user registration, posting photos, commenting, liking, and following other users based on the database schema.
- Testing: Thoroughly test the application to ensure all functionalities work as expected and data is correctly stored and retrieved from the database.

## Notes
- Ensure proper data types, indexes, and foreign key constraints are applied to maintain data integrity and optimize database performance.
- Periodically backup the database to prevent data loss.
- Customize and extend the database schema as needed to meet specific requirements.
