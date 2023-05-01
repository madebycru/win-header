## WIN 3D Header

This github repository holds all 3D Header that are used on the win-ci.com website. Below it's explained how to upload new header or update existing ones.

\

\

## Overview

1. Access to Repository
2. Folder Structure
3. Prepare header images
4. Upload header images
5. Set header images in primic (CMS)
6. Update already uploaded header images

\
\


## 1. Access to Repository

To upload headers, you need access to this repository. (https://github.com/madebycru/win). Currently only jonathan@madebycru.com can invite to it, however this will be changed.

\

\


## 2. Folder Structure

The images are structured into the two folders desktop and mobile. 

Difference is the image size:
- Desktop: 1024px x 1024px
- Mobile: 512px x 512px

Within these folders we have the folder png and webp. In those we have the folders with the sequences, with images in type png and webp. 

For the website we **ONLY** use webp due to loading times. Therefore the webp files **ALWAYS** need to be uploaded.


```

├── desktop
|   |
|   └── png
|       └── {header_name}
|       	└── {header_name}_00000.png
|   |
|   └──webp
|       └── {header_name}
|       	└── {header_name}_00000.webp
|
|
|
├── mobile
|   |
|   └── png
|       └── {header_name}
|       	└── {header_name}_00000.png
|   |
|   └──webp
|       └── {header_name}
|       	└── {header_name}_00000.webp
|     
|
├── README.md
```

\

\

## 3.Prepare header images

Before uploading the headers, we need the sequence in to sizes:
- 1024px x 1024px
- 512px x 512px

Both sequences need to be converted to webp. Each image in the sequence should have a file size between 10KB and 30KB. The small, the better.


The name of the images need to be exactly like the folder name + ```_00000.webp```. 

As an example:
- Folder name: ```_client_name```
- File names: ```_client_name_00000.webp``` ```_client_name_00001.webp``` ...


\
\

## 4. Upload header images

- Withing the win-header github navigate to the correct folder. 
	- Example: /desktop/webp
- Click on Add File -> Upload Files
- Drag and drop the whole Folder with the images in it.
- After uploading click on Commit changes

Do this for mobile and desktop.


\

\

## 5. Set header images in primic (CMS)

To set the header images somewhere on the website you have to login to prismic and navigate to a case and select the tab "3D Teaser".

You need to do 2 things:

- In the field ```Product Shot``` add the **exact** folder name of the header
- In the field ```Product Shot Frame Count``` add the number of frames.
- Click save and publish.

\

\


## 6. Update already uploaded header images

To replace existing images just do step **4**. After uploading and commiting the images are replaced. However you will not see them on the website yet. 
To do so you have to generate the page again:

- In **madebycru/win-header** github click on the tab **Actions**
- Choose **Netlify Deploy**
- Click **Run workflow** with Branch Main selected.
- Wait a few minutes. 


**Keep in mind:** To replace a header, the folder name and file names need to be exactly the same. Also don't forget to replace it for desktop on mobile, in case both changed.
