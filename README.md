<p align="center">
  <a href="https://github.com/x0sina/marzban-sub" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/x0sina/marzban-sub/main/PreviewTemplate.png" alt="Marzba-Sub" title="Marzba-Sub"/>
  </a>
</p>

<h1 align="center">Subscription Template for <a href="https://github.com/Gozargah/Marzban">Marzban</a></h1>

## Table of Contents
- [Introduction](#introduction)
- [Attributes](#attributes)
- [Installation Steps](#installation-steps)
- [Default Language](#default-language)
- [Personalization](#personalization)
- [Host Version](#host-version)
- [Copyright](#copyright)

# Introduction
Enhance user information display with this simple HTML template.

# Attributes
- Easily integrate subscription links into programs
- Download links for required applications
- Supports three languages: Russian, English, Persian
- Visually appealing fantasy page with beautiful colors
- Configurations can be copied with the icon at the bottom of the page

# Installation Steps
1. Download the Template File:
```sh
sudo wget -N -P /var/lib/marzban/templates/subscription/  https://raw.githubusercontent.com/codedpro/marzban-sub/main/index.html
```

2. Configure Marzban:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```
Alternatively, uncomment the following values in the `.env` file located in the `/opt/marzban` folder by removing the # at the beginning of each line:
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

3. Restart Marzban:
```sh
marzban restart
```

## Update
To update the template, repeat step 1.

# Default Language
To change the default language, locate the select tag at the end of the HTML file and modify the desired language option. For example:
```
<select id="countries" class="border text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white :focus:ring-blue-500 :focus:border blue-500">
  <option value="en">English</option>
  <option value="fa">فارسی</option>
  <option value="ru">Русский</option>
</select>
```
In this example, English is the default language.

# Personalization
To personalize the Telegram ID, background image, and user logo, make changes directly in the HTML file. Use the following search phrases with a text editor like nano:
- To change the Telegram support ID:
```
https://t.me/yourID
```
- To change the user's logo:
```
images/marzban.svg
```
- To change the background image:
```
background: url('https://4kwallpapers.com
```
After making changes, save the file and restart Marzban.

## Host Version
For the hosted version, upload the 'sub' folder to your host and adjust the BASE_URL value in the 'index.php' file accordingly, as shown in the example:
```
const BASE_URL = "https://BaseUrl:PORT";
```

## Copyright
This template is based on <a href="https://github.com/Gozargah/Marzban">Marzban Templates</a> design.
```

This single README.md file contains all the information you provided in the initial document, structured and formatted for clear readability and comprehension.
