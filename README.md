from gethund import GethundClient

# Replace with your actual Gethund API key
api_key = "YOUR_GETHUND_API_KEY"

# Create a Gethund client
client = GethundClient(api_key=api_key)

# Define the profile data
profile_data = {
    "username": "DataDynamo",  # Or a more creative username
    "bio": "Data Scientist | Transforming raw data into strategic insights. Passionate about machine learning, AI, and unlocking the stories hidden within datasets. Let's connect and innovate!",
    "location": "Global (Remote-Friendly)",  # Or your specific city
    "website": "https://your-portfolio-website.com",  # Replace with your portfolio
    "twitter_handle": "@DataInsightsPro",  # Or your handle
    "github_username": "DataExplorer",  # Or your GitHub username
    "skills": [
        "Python (Pandas, Scikit-learn, TensorFlow, PyTorch)",
        "SQL",
        "Machine Learning (Regression, Classification, Clustering)",
        "Deep Learning (CNNs, RNNs)",
        "Data Visualization (Tableau, Power BI, Matplotlib, Seaborn)",
        "Statistical Analysis",
        "Big Data (Spark, Hadoop - if applicable)",
        "Cloud Computing (AWS, Azure, GCP - if applicable)",
        "Natural Language Processing (NLP)",
        "Time Series Analysis"
    ],
    "interests": [
        "Artificial Intelligence",
        "Machine Learning Ethics",
        "Data-Driven Storytelling",
        "Predictive Modeling",
        "Data Visualization for Impact",
        "Open Source Data Science",
        "Cutting-Edge AI Research"
    ],
    "experience": [
        {
            "company": "Hexaware Technologies", #Or your company
            "title": "Rising Star - Data Analyst/Aspiring Data Scientist", #Or your current role
            "start_date": "YYYY-MM-DD",
            "end_date": "Present",
            "description": "Demonstrated rapid learning and adaptability, earning the 'Rising Star' award. Honed analytical skills, data manipulation, and reporting. Currently transitioning to a data science role by actively developing machine learning and data visualization expertise."
        },
        # Add more experience entries as needed
    ],
    "education": [
        {
            "institution": "Your University Name", #Or your university
            "degree": "Bachelor of Computer Applications (BCA)",
            "major": "Computer Applications",
            "graduation_date": "YYYY-MM-DD"
        },
        # Add more education entries as needed
    ],
    "projects": [
        {
            "name": "Customer Churn Prediction Model",
            "description": "Developed a machine learning model using Python (Scikit-learn) to predict customer churn, achieving [quantifiable result] accuracy. Code and analysis available on GitHub.",
            "link": "https://github.com/DataExplorer/churn-prediction"  # Replace with your project link
        },
        {
            "name": "Interactive Data Visualization Dashboard",
            "description": "Created an interactive dashboard using Tableau/Power BI to visualize key performance indicators, providing actionable insights for stakeholders.",
            "link": "https://your-portfolio-website.com/dashboard" #Replace with your project link
        },
        # Add more project entries as needed
    ]
}

# Create the profile
try:
    response = client.create_profile(profile_data)
    print(f"Profile created successfully! Profile ID: {response['id']}")
except Exception as e:
    print(f"Error creating profile: {e}")
