# E-commerce Website-SCV Auto

## Overview
This project is a comprehensive e-commerce web application designed to provide users with a seamless shopping experience. The application incorporates various modern web technologies to ensure responsiveness, user-friendliness, and efficiency.

## Technologies Used
- **HTML**: For structuring the web pages.
- **CSS**: For styling and layout.
- **Bootstrap**: For responsive design and quick styling.
- **JavaScript**: For interactive elements and functionality.
- **PHP**: For server-side scripting and database interaction.
- **MySQL**: For managing the database.

## Features
- **User Authentication**: Secure login and registration system.
- **Product Management**: Admin interface for adding, updating, and deleting products.
- **Shopping Cart**: Add to cart functionality with session management.
- **Search Functionality**: Search for products by name.
- **Responsive Design**: Accessible on various devices and screen sizes.

## Installation
To set up the project on your local machine (for the purpose of this demo i used AWS VM EC2 instance/ Ubuntu Server 24.04), follow these steps:

### Install Dependencies:
Ensure you have a **LAMP stack** installed in Windows OS (Linux, Apache, MySQL, PHP) or **XAMPP stack** for linux OS.
### Download XAMPP:
Go to the XAMPP download page and download the Linux version. Alternatively, you can use `wget` to download it directly to your server:
```bash
wget https://sourceforge.net/projects/xampp/files/XAMPP%20Linux/8.0.30/xampp-linux-x64-8.0.30-0-installer.run
```
![image](https://github.com/sterevirgil29/XAMPP---Ecommerce-web-based-application/assets/151761670/b0cec4d0-7b53-4bc4-b1b4-0e733029fff2)

Make sure to check the latest version and replace the URL with the appropriate one if necessary.

### Make the Installer Executable:
Change the permissions of the downloaded file to make it executable:
```bash
chmod +x xampp-linux-x64-8.0.7-0-installer.run
```
![image](https://github.com/sterevirgil29/XAMPP---Ecommerce-web-based-application/assets/151761670/76cd9d1a-da0d-46f8-a6bc-054c3f45c078)

### Run the Installer:
Execute the installer:
```bash
sudo ./xampp-linux-x64-8.0.7-0-installer.run
```
### Start XAMPP:
After the installation is complete, you can start XAMPP using the following command:
```bash
sudo /opt/lampp/lampp start
```
![image](https://github.com/sterevirgil29/XAMPP---Ecommerce-web-based-application/assets/151761670/9a8c97ef-8f07-40d9-8fa5-d8ea2a1af493)

  ### Clone the Repository (move to the XAMPP root install before cloning the repo):
```bash
git clone https://github.com/your-username/XAMPP---Ecommerce-web-based-application.git
```
### Navigate to the Project Directory:
```bash
cd XAMPP---Ecommerce-web-based-application
```
### Set Up the Database:
- Allow Phpmyadmin remote access by removig the security feature (for the moment)
  ```bash
  cd /opt/lampp/etc/extra$
  sudo nano httpd-xampp.conf
  ```
  - Modify this
    ```bash
    <Directory "/opt/lampp/phpmyadmin">
    AllowOverride AuthConfig Limit
    Require all granted
    ErrorDocument 403 /error/XAMPP_FORBIDDEN.html.var
    </Directory>
   ``` 

- Create a **MySQL database**.
- Import the provided SQL file to set up the necessary tables:
  ```bash
  mysql -u username -p database_name < database.sql
  ```

  ### Configure the Application:
Update the database configuration in `lib/connection.php` with your **MySQL credentials**.

### Start the Server:
Ensure **Apache** is running:
```bash
sudo service apache2 start
```
### Access the Application:
Open your web browser and navigate to `http://localhost/XAMPP---Ecommerce-web-based-application`.

## Usage
- **User Registration and Login**: Users can register and log in to access their profiles.
- **Browse Products**: Users can view all available products.
- **Add to Cart**: Logged-in users can add products to their cart.
- **Checkout**: Users can view their cart and proceed to checkout.

## Contributing
We welcome contributions to enhance the functionality and features of this project. Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

## License
This project is licensed under the **MIT License**. See the LICENSE file for details.

## Acknowledgements
- **Bootstrap**
- **Google Fonts**
- **Font Awesome**
