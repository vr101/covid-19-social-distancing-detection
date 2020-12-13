# covid-19-social-distancing-detection

ABSTRACT
COVID-19, caused by a novel virus, the coronavirus or SARS-CoV-2 is a respiratory illness
that has become a pandemic.
This virus, first detected in Wuhan, Hubei Province, China has spread across the world in more
than 180 countries, resulting in 26.3 million confirmed cases along with 870,000 deaths as on
September 4, 2020.
The reason that COVID 19 is so dangerous is that it can spread through droplets or even stay
in the air as an aerosol making it impossible to detect. The other factor is that many carriers of
the disease may be asymptomatic so they may not take the precautions necessary to not spread
the disease. The lack of any active therapeutic agents and the lack of immunity against COVID
19 increases the vulnerability of the population. Since there are no vaccines available as of
now, social distancing is the only feasible approach to fight against this pandemic.
Social distancing means any measures taken to increase physical space between people to slow
or prevent the spread of the virus. This involves avoiding public gatherings, limiting the
number of visitors at home, staying at home more often, keeping a safe distance from other
people and catching up with friends and family virtually instead of in person.
If you have to be around people, maintain a distance of 2 meters or 6 feet from others around
you as much as possible.

However, individuals are not used to tracking the required 6-feet (2-meters) distance
between themselves and their surroundings.
To tackle the highlighted issue, this project proposes a deep learning based model for
automating the task of monitoring social distancing using surveillance video.
OBJECTIVES
The aim of this project is
• to incorporate a deep learning-based real-time object detector into a a monocular camera to
measure social distancing and to ensure that,
• to ensure system should never record/cache data
• to ensure the warnings should not target the individuals, rather a breach occurring.
The proposed framework utilizes the detectron2 object detection model to segregate humans
from the background and Deepsort approach to track the identified people with the help of
bounding boxes and assigned IDs.
The distance between any two persons is computed. The major issue while calculating this
distance is that working with the point of view of the surveilla006Ece cameras does not provide
us with a bird's eye view, rather a skewed view from the angle at which the camera is placed.
This hampers the calculations and leads us to incorrect evaluation.
In order to rectify this issue, we have taken the help of the warptransform() function which
works in a way so as to map the skewed video and transform the coordinates, convert the 3D
imagery so as to help us achieve a bird's eye view.
As long as safe distance is maintained between any two persons the bounding box is blue in
colour. If the distance is less than 6-feet, the model returns a red bounding box and sends an
alert without targeting the individual who breached the social distancing measure.
