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
- Repository link: https://github.com/njaideep2003/moments-CS594-Homework-1
- Latest commit link: https://github.com/njaideep2003/moments-CS594-Homework-1/commit/4956dbdf0c55223c7340c46dc98c6e909351d3d4

## Installation Process:
### 1. Clone the Project  
```bash
git clone https://github.com/njaideep2003/moments-CS594-Homework-1.git
cd moments
```

### 2. Set Up a Virtual Environment  

For macOS/Linux:  
```sh
python3 -m venv myenv  
source myenv/bin/activate  
```  

For Windows:  
```sh
python -m venv myenv  
myenv\Scripts\activate  
```  

### 3. Install Dependencies  
```sh
pip install -r requirements.txt  
```

## Setting up the API Key
Moments relies on **Azure Vision API** to analyze images. Here’s how to connect it:  

1. **Create an Azure Computer Vision account**  
   - Sign up at your Azure Portal. 
   - Generate an API Key and Endpoint URL  

2. **Save your credentials securely**  
   - In your root directory, create a `.env` file:  
     ```sh
     AZURE_VISION_API_KEY="your-api-key-here"  
     AZURE_VISION_ENDPOINT="your-endpoint-here"  
     ```  
   - Keep this file private—it should never be pushed to GitHub. 

## Run the App Locally  

To start the Flask server, run:  
```sh
flask run  
```  

Then, open:  
[http://127.0.0.1:5000](http://127.0.0.1:5000)  

## How to Use Moments  

### Upload and Organize the Photos  
1. Click "Upload"  
2. Select an image  
3. AI automatically generates alt text and searchable tags  

### Find Photos Instantly  
- Type a keyword into the search bar to find images based on AI-generated tags  
- Example: Searching "cars" will show all beach-related photos  

### Edit and Customize the Tags  
- Open an image  
- Click "Add Tags"  
- Enter custom tags and save them 

### Check AI-Generated Descriptions  
- Right-click an image → Click "Inspect Element"  
- Locate the `<img>` tag to see the **alt attribute**  

## Given demo account

Use this to login and explore:  

- **Email:** admin@helloflask.com  
- **Password:** moments 

## Technologies used

- **Python & Flask** – backend work  
- **SQLAlchemy** – database management  
- **Azure Vision API** – AI-powered image recognition  
- **Bootstrap 5** – Frontend work 
- **WTForms** – Secure form handling  
- **Flask-Login** – Authentication and session management

## Potential Harms

### Incorrct Image description
- problem: AI might not identify objects correctly and give inaccurate descriptions.
- solution: users can manually edit the AI generated description.

### Bias in AI Recognition
- problem: AI models may not be equally accurate across all demographics due to the model training.
- solution: Manual tagging allows users to refine and correct the results.

### Scalability
- problem: Too many uploads at a time can slow API performance.
- solution: Implement caching and background processing for smooth performance.

### security practices
- credentials such as api keys shouldn't be committed to GitHub.
- Sanitization & validation for user inputs.
- All sensitive data is managed through environment variables.

### Future Developments
- Optimize API Calls: Batch process images for better efficiency.
- Scalability Enhancements: change to cloud-based infrastructure for best performance.
- Better Tag Management - Improve AI tagging accuracy by model training.

## Production Challenges
1. cost of operation
- problem: Frequent API calls might increase the cost over time.
- solution: Reducing unnecessary API requests by storing AI-generated tags in the database.
  
2. Infrastructure
- problem: Hosting a huge number of images increases the storage requirements.
- solution: Use cloud storage services like AWS/Google cloud/Azure storage

## contributor
- **Jaideep Nutalapati**
- **jnuta@uic.edu**
- Github link: https://github.com/njaideep2003
