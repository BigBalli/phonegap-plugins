*********************** 
add the event listener to know when the orientation changes

document.addEventListener("orientationChanged", function() { 
                                        PhoneGap.exec("NativeControls.updateTabBar"); 
                                        }, false); 
************************ 
In setupToolbars() (in your javascript) substitute window.uicontrols.showTabBar(); with 
PhoneGap.exec("NativeControls.updateTabBar"); so that there would be no 
issues with the famous 20px (in my case, and I believe most, the 
status bar is visible). 
As you can see all the values are hard coded. Although it accounts for 
all orientations of iPhone and iPad I understand that for a cleaner 
coding etiquette someone might want to use variable etc. Feel free. 
The point was to make it work and it does, like a charm. 