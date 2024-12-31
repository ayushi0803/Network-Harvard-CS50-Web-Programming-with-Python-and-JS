```markdown
# CS50 Web Programming with Python and JavaScript: Network Project

This is the Network project for CS50's Web Programming with Python and JavaScript course, where you will design a social network similar to Threads that allows users to post updates, follow others, and "like" posts. The project uses Python (Django), JavaScript, HTML, and CSS.

## Table of Contents
- [Overview](#overview)
- [Getting Started](#getting-started)
- [Project Specification](#project-specification)
- [Hints](#hints)
- [How to Submit](#how-to-submit)
- [Setup](#setup)

## Overview

This project involves the development of a social network with the following features:
- **New Post**: Users can create text-based posts.
- **All Posts**: Displays posts from all users with pagination.
- **Profile Page**: Displays the user's profile, their posts, and the number of followers/following.
- **Following**: Users can follow other users and view posts from those they follow.
- **Edit Post**: Users can edit their own posts.
- **Like/Unlike Posts**: Users can like or unlike posts.

The backend is implemented in Django, with frontend components in HTML, CSS, and JavaScript.

## Getting Started

### 1. Download the Distribution Code

First, download the distribution code:
- [CS50 Network Distribution](https://cdn.cs50.net/web/2020/spring/projects/4/network.zip)

Unzip the downloaded file and navigate into the project directory.

### 2. Install Dependencies

If you haven't already, make sure you have Python and Git installed. It's also recommended to create a virtual environment.

In the terminal, run:

```bash
pip install -r requirements.txt
```

### 3. Initialize the Database

Run the following commands to create the database tables:

```bash
python manage.py makemigrations network
python manage.py migrate
```

### 4. Run the Development Server

Start the Django development server:

```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` in your browser to start using the application.

### 5. Register a User Account

Click "Register" to create an account. Once registered, you can sign in and start using the social network.

## Project Specification

The following features are required for the project:

### 1. New Post

- Users must be able to write a new text-based post and submit it.
- The post will be displayed on the "All Posts" page.

### 2. All Posts

- The "All Posts" page should display posts from all users, with the most recent first.
- Each post should include the username, content, date/time, and like count.

### 3. Profile Page

- Clicking on a username should take the user to their profile page.
- The profile page should display the number of followers and following, along with the user's posts.
- Other users can follow/unfollow the user (but not themselves).

### 4. Following

- The "Following" page shows posts from users the current user follows.
- This page should be available only to authenticated users.

### 5. Pagination

- Posts should be paginated, with a maximum of 10 posts per page.
- "Next" and "Previous" buttons should be available to navigate between pages of posts.

### 6. Edit Post

- Users should be able to edit their own posts without reloading the page.
- Only the post's author should be able to edit the post.

### 7. Like and Unlike

- Users can toggle likes on posts.
- Likes should be asynchronously updated without page reload using JavaScript's `fetch`.

## Hints

- Use Django’s built-in pagination for handling post pagination.
- Implement asynchronous operations (e.g., for liking posts) using JavaScript and `fetch`.
- Ensure your models in `network/models.py` represent the necessary data structures (posts, likes, followers, etc.).
- Bootstrap is used for frontend design, but feel free to customize it.
- For the profile page, display posts in reverse chronological order.

## How to Submit

### 1. Organize the Project

Ensure your project’s file structure matches the following:

```
network/
  manage.py
  network/
    migrations/
    models.py
    views.py
    templates/
    static/
```

### 2. Submit via GitHub

- Push your code to GitHub under the branch `web50/projects/2020/x/network`.
- Record a screencast (max 5 minutes) demonstrating all functionality.
- Upload your screencast to YouTube (unlisted or public, but not private).
- Ensure your video description includes timestamps for each element of the specification.

### 3. Submit via `submit50`

You can submit your project using:

```bash
submit50 web50/projects/2020/x/network
```

Alternatively, push your work to GitHub and submit the link through the CS50 submission form.

## Setup

1. **Install Python and Git**: Ensure Python and Git are installed on your system.
2. **Clone the Repository**:

```bash
git clone https://github.com/kazimovzaman2/CS50w-Network.git
cd cs50w_network
```

3. **Install Dependencies**:

```bash
pip install -r requirements.txt
```

4. **Initialize the Database**:

```bash
python manage.py makemigrations network
python manage.py migrate
```

5. **Run the Development Server**:

```bash
python manage.py runserver
```

## License

This project is part of CS50's Web Programming with Python and JavaScript course, offered by Harvard University.

---

For more information about the course and other resources, visit [CS50 Web Programming](https://cs50.harvard.edu/web/2020/).

