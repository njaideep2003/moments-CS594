# CS 594 – Responsible AI Engineering
# Homework 1: Building an ML-enabled Product using Moments
Moments is an image-sharing platform built with Flask that uses AI to enhance accessibility and searchability. With the help of the Azure Vision API, it automatically generates alternative text and tags for images, making it easier to find and use them.

## Features
- **AI Generated Alt Text** - It automatically adds the descriptions to images for better accessibility.  
- **Smart Image Tagging** - AI identifies objects in the images and stores them as searchable tags.   
- **Image Searching** - Users can search images with the help of AI-generated tags.  
- **Custom Tags** - Users can manually add or edit tags.  
- **User Authentication** - Manage profiles with safe login and authentication. 
- **Image Sharing & Engagement** - Share and engage with the photos online.

## How AI describes the Images
After a photo is uploaded, the Microsoft Azure Vision API examines it and creates a useful description. For quick and effective searches, this AI-generated alt text is thereafter saved in the database. The description can be changed or replaced before to publication. To ensure accessibility for all users, an alt attribute is automatically included with every image.

## AI Makes Searching easy
Moments makes image search simple, so spending time browsing to discover a picture will be decreased. Every uploaded image is scanned by AI, which then identifies items and applies pertinent tags. Because these tags are stored in the database, a quick keyword search will help you locate photographs required.
Example: Searching for "cars" will instantly show all images containing cars without needing to tag or search them manually.

## User Interface design 
- **Alt text:** AI generates the descriptions based on the images, but you can edit them manually.
- **Image searching:** AI automatically generates tags for each image, such that we can search by keywords, and matching images appear in no time.

## Github link and Commit link:
