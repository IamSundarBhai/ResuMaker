
---

# **System Requirements Document**  
### **Project Name**: ResuMaker (AI Resume Generator)  
### **Version**: 1.0  
### **Date**: 27-Feb-2025  

---

## **1. Overview**  
**ResuMaker** is an AI-powered resume generator that helps users create professional, **ATS-friendly** resumes instantly. It leverages **OpenAI's GPT-4 API** for generating content and uses **.NET technologies** for backend processing, UI, and PDF generation.  

---

## **2. Functional Requirements**  

### **2.1 Core Features**  
✅ **User Input & Profile Setup**  
- Users enter details: **Name, Job Title, Experience, Skills, Contact Info**  
- Option to **upload an existing resume** for AI enhancement  

✅ **AI-Powered Resume Generation**  
- Uses **GPT-4 Turbo** to generate professional resume content  
- Provides **multiple resume formats** (chronological, functional, hybrid)  
- ATS-optimized resume suggestions  

✅ **Resume Editing & Customization**  
- Users can edit **AI-generated content**  
- Customizable **font styles, layouts, colors, and sections**  

✅ **Export & Sharing**  
- Converts resumes to **PDF, DOCX**  
- Share resume via **email or direct link**  
- Optional **cloud storage** for saving resumes  

✅ **User Authentication (Optional)**  
- **Google & Email Login** for personalized experience  
- Securely store **previously generated resumes**  

✅ **Dashboard & Resume Management**  
- View, edit, or delete **previously created resumes**  
- Download history and analytics  

✅ **Job Matching & AI Suggestions (Future Feature)**  
- AI-powered **job recommendations** based on resume content  
- AI-driven **resume improvement suggestions**  

---

## **3. Non-Functional Requirements**  

### **3.1 Performance**  
- Resume generation should **complete in under 5 seconds**  
- PDF export should take **less than 3 seconds**  
- Supports **1000+ concurrent users**  

### **3.2 Security**  
- **User data encryption** for privacy (AES-256)  
- **Secure API Key management** for OpenAI & cloud storage  
- **OAuth2 authentication** for user accounts  

### **3.3 Scalability**  
- **Cloud-based hosting** for high availability (Azure, AWS)  
- **Load balancing** to handle large traffic  
- **Microservices architecture** for future expansion  

### **3.4 Availability**  
- **99.9% uptime guarantee**  
- **Auto-retry mechanisms** for API failures  

---

## **4. Technical Requirements**  

### **4.1 Software Requirements**  
| Component        | Description |
|-----------------|------------|
| **Programming Language** | C# (.NET 7/8) |
| **Backend Framework** | ASP.NET Core Web API |
| **Frontend Framework** | Blazor / React.js (Optional) |
| **Database** | SQL Server / PostgreSQL / MongoDB (Optional) |
| **AI Integration** | OpenAI GPT-4 API |
| **Authentication** | IdentityServer, OAuth2 |
| **PDF Generation** | iTextSharp (.NET PDF Library) |
| **Cloud Storage** | Azure Blob, AWS S3 (Optional) |

### **4.2 Hardware Requirements**  
| Component        | Minimum Requirement | Recommended |
|-----------------|--------------------|-------------|
| **Processor** | Intel i3 or AMD Ryzen 3 | Intel i5/i7 or AMD Ryzen 5/7 |
| **RAM** | 4GB | 8GB+ |
| **Storage** | 20GB free space | SSD for faster processing |
| **Internet** | Required (for API calls) | High-speed connection |

---

## **5. API Requirements**  
| API | Purpose |
|-----|---------|
| **OpenAI GPT-4 API** | Resume text generation |
| **iTextSharp** | PDF generation |
| **Google Drive API (Optional)** | Resume cloud storage |
| **Twilio API (Optional)** | Resume sharing via SMS/Email |

---

## **6. Deployment Requirements**  

### **6.1 Local Development**  
- **OS**: Windows 10/11 or macOS/Linux  
- **Tools**: Visual Studio 2022, .NET SDK 7/8  
- **Database**: SQL Server (LocalDB), PostgreSQL  

### **6.2 Cloud Deployment**  
- **Hosting**: Azure App Service, AWS Lambda, or Google Cloud Run  
- **CI/CD**: GitHub Actions, Azure DevOps  
- **Database**: Azure SQL, Firebase, or MongoDB Atlas  

---

## **7. User Roles & Access Control**  

| User Role | Permissions |
|-----------|------------|
| **Guest** | Generate resumes (No save history) |
| **Registered User** | Save, edit, and manage resumes |
| **Admin** | Manage users, templates, and analytics |

---

## **8. Future Enhancements** (Version 2.0+)  
✅ **AI-powered Resume Feedback** (Score and suggestions for improvement)  
✅ **Job Matching** (Connects users to job openings based on resume)  
✅ **LinkedIn Integration** (Import user data from LinkedIn)  
✅ **Mobile App** (Android & iOS version for resume creation on the go)  

---

## **9. Conclusion**  
**ResuMaker** will be a **fast, AI-powered resume builder** built on **.NET** with advanced **resume customization, export, and job-matching features**. It will be **scalable, secure, and optimized for ATS systems**, helping job seekers create **professional resumes effortlessly**.  

---

## **1. Backend (API & Business Logic)**
| **Technology** | **Why Use It?** |
|--------------|-------------|
| **.NET 7/8 (ASP.NET Core Web API)** | High performance, scalable, and modern framework for web applications |
| **C#** | Strongly-typed, fast, and ideal for enterprise applications |
| **Entity Framework Core** | ORM for easy database interactions |
| **MediatR (CQRS Pattern)** | Improves API scalability and maintainability |
| **Serilog** | Structured logging for debugging and monitoring |

---

## **2. AI Integration**
| **Technology** | **Purpose** |
|--------------|-------------|
| **OpenAI GPT-4 API** | AI-generated resume content |
| **LangChain.NET** | For enhanced AI prompt engineering & processing |
| **Azure OpenAI / OpenAI SDK** | Alternative AI provider for security & enterprise integration |

---

## **3. Database (Storage)**
| **Database** | **Why Use It?** |
|-------------|----------------|
| **SQL Server / PostgreSQL** | Relational database for structured resume storage |
| **MongoDB (Optional)** | NoSQL for flexible document storage (if needed for user profiles) |
| **Azure Cosmos DB** | Scalable cloud-based database (NoSQL) |
| **Redis** | Caching layer for improved performance |

---

## **4. Frontend (User Interface)**
| **Technology** | **Why Use It?** |
|--------------|-------------|
| **Blazor (WASM or Server)** | Native .NET frontend with high performance |
| **React.js (Optional)** | If you prefer a JavaScript-based UI |
| **Tailwind CSS / Bootstrap** | Modern, responsive UI design |
| **ShadCN UI** | Pre-built UI components for professional design |

---

## **5. PDF Generation & File Handling**
| **Technology** | **Why Use It?** |
|--------------|-------------|
| **iTextSharp / QuestPDF** | Generate professional resumes in PDF format |
| **DocX (OpenXML SDK)** | Word document support for resumes |
| **Azure Blob Storage / AWS S3** | Cloud storage for generated resumes |

---

## **6. Authentication & Security**
| **Technology** | **Why Use It?** |
|--------------|-------------|
| **IdentityServer4** | Secure OAuth2 authentication |
| **Azure AD B2C / Google Auth** | Social login options |
| **JWT (JSON Web Tokens)** | Secure API authentication |
| **AES-256 Encryption** | Protects user data |

---

## **7. Deployment & DevOps**
| **Technology** | **Why Use It?** |
|--------------|-------------|
| **Azure App Service / AWS Lambda** | Cloud hosting for API |
| **Docker & Kubernetes** | For containerization & scalability |
| **GitHub Actions / Azure DevOps** | CI/CD pipeline automation |
| **Terraform** | Infrastructure as Code (IaC) |

---

### **Prototype Screens**

User Registration

![Registration Page](https://github.com/user-attachments/assets/eb5e023f-5362-4651-ae67-ec56d2133ff8)

Login Page 
![Login Page](https://github.com/user-attachments/assets/de401162-dc8b-4cc3-86f4-103bb6f4946c)


---

### **🔥 Best Stack for ResuMaker (Recommended)**
✅ **Backend:** ASP.NET Core (.NET 8) + C#  
✅ **Frontend:** Blazor (or React.js) + Tailwind CSS  
✅ **Database:** PostgreSQL (or SQL Server)  
✅ **AI:** OpenAI GPT-4 + LangChain.NET  
✅ **PDF Handling:** iTextSharp / QuestPDF  
✅ **Hosting:** Azure App Service + Docker  

---
