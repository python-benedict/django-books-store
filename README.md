# django-books-store
This is a django ecommerce books shop


STEPS TO CREATE A MEDIA FILE (LINK YOUR IMAGES OR VIDEOS)
1. in your product file add a field call images and in therer write -->> images = modes.ImageField(upload_to=('images/'), where the images/ is where the images you uploads will be save to.
2. after that creat a folder called media in the base directory
3. go to the settings and add this things below.
a. MEDIA_URL = '/media/'
b.MEDIA_ROOT = os.path.join(BASE_DIR, 'media/')

4. Go to urls.py in your project directory and add the following to it or in other words import
a. from django.conf import settings
b. from django.conf.urls.static import static

if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
