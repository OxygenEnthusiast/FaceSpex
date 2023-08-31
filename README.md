# FaceSpex

FaceSpex empowers users to effortlessly generate high-quality facial images with precisely
definable superficial attributes, such as trustworthiness, attractiveness, and more. 

## Description

FaceSpex utilizes survey data from a study by J.C. Peterson and colleagues,
which is accessible
[here](https://github.com/jcpeterson/omi).
In this
research, participants rated facial features based on various attributes,
resulting in corresponding ratings. FaceSpex uses these ratings to generate
images representing specific perceived attributes.
The available attributes
include:
'trustworthy', 'attractive', 'dominant', 'smart', 'age', 'gender', 'weight',
'typical', 'happy', 'familiar', 'outgoing', 'memorable', 'well-groomed',
'long-haired', 'smug', 'dorky', 'skin-color', 'hair-color', 'alert', 'cute',
'privileged', 'liberal', 'asian', 'middle-eastern', 'hispanic', 'islander',
'native', 'black', 'white', 'looks-like-you', 'gay', 'electable', 'godly'
and 'outdoors'.

## Highlights

- Easily generate High definition images using google colab and save them 
    to google drive.
- Control up to 34 superficial attributes
- Control one attribute while keeping another one stable.
- All code in a single Notebook. So it is easy to read for non-programmers.

## Limitations

- Only control a single attribute.
- Only stabilize a single attribute.
- Since the code is in a notebook it is not easy to expand.


## Setup instructions

For a much quicker installation, you can download pregenerated data.

To do that: 

1. Download the gen_faces/attr_dirs.pkl file from this repo. (Click
    [here](https://github.com/OxygenEnthusiast/generate_faces/raw/main/gen_faces/attr_dirs.pkl))
2. Log into google drive
3. Create a folder called gen_faces in the base folder of your google drive.
4. Put the attr_dirs.pkl file into the created folder.

### Calculate the directions yourself (not recommended)

If you want to project the latent vectors and/or generate the 
attribute directions yourself, you can download the 
entire gen_faces directory. Then you delete attr_dirs.pkl as well as the "l_vecs"
directory.
Note that projecting the images can take up to 2 days, generating the 
directions takes ~15 minutes.

## Usage 

To run the script open 
[gen_faces.ipynb](https://github.com/OxygenEnthusiast/generate_faces/blob/main/gen_face.ipynb)
and click ''open on colab'' on top of the notebook.
In colab sign in with the google account you used 
for the google drive. To connect your google drive click on ''files'' and then click 
''Mont Drive''. You should now be able to use the notebook. Feel free 
to change the form fields. To run the notebook you can click on 
''Runtime'' -> ''Run all''. To save time you can simply run the last
cell (''Main Code'') for any subsequent runs.

## Possible improvements.

- Control and stabilize multiple attributes.
- First generate base images, then select interesting ones and then use only
    the selected images for manipulation.
- Use real images as base images (face to face manipulation).
- When calculating the empirical 
    mean and standard deviation, use a set of images more representative of the
    human population.

## Credits

This Project would not have been possible without 
[J.C. Petersons One Million Impressions Dataset](https://github.com/jcpeterson/omi)
and
[StyleGAN2-ada](https://github.com/NVlabs/stylegan2-ada-pytorch).
Special Credit goes to the paper by Peterson et al. titled 
"Deep models of superficial face judgment" where most of the ideas 
used here are described.

## License?

Since both the
[omi-dataset license](https://github.com/jcpeterson/omi/blob/main/LICENSE.txt)
and
[StyleGAN license](https://github.com/NVlabs/stylegan2-ada-pytorch/blob/main/LICENSE.txt)
are non-commercial,
I have no idea what license to use to make my work open source.

Feel free to suggest changes and 
use this code yourself.
