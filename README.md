# Baikal plankton image dataset
Dataset contains microscope images of various plankton species from lake Baikal.


[Medium article about our work and how dataset is obtained.](https://medium.com/yandex/surveying-the-microogranisms-of-lake-baikal-an-open-project-by-maritimeai-and-yandex-cloud-83999a4def36)


Images are obtained from microscope camera with same image background and backlight.

We provide polygonal labeling for object detection, segmentation and classification tasks.
Currently, we provide images 72 different species as well as category `other` for image artefacts, background, etc.

<!-- 
Full list of classes:

<summary>

* cladocera
* daphnia longispina
* epischura baikalensis nauplii stage 1
* epischura baikalensis copepoda stage 4
* bosmina longirostris adult
* epischura baikalensis copepoda stage 1
* epischura baikalensis egg
* cyclops baicalensis copepoda 2 stage
* epischura baikalensis copepoda stage 2
* epischura baikalensis nauplii stage 5
* cyclops kolensis copepoda stage 1-2
* epischura baikalensis nauplii
* eggs
* gastropus stylifer
* keratella quadrata with egg
* pinus seed
* filamentous algae
* epischura baikalensis copepoda stage 3
* epischura baikalensis nauplii stage 4
* macrohectopus branickii
* keratella cochlearis
* synchaeta stylata
* collotheca mutabilis without egg
* epischura baikalensis copepoda
* synedra acus
* keratella quadrata without egg
* cyclotella minuta
* notholca grandis without egg
* collotheca
* cyclops kolensis copepoda stage 3
* epischura baikalensis adult female
* rotifera
* cyclops kolensis male
* cyclops kolensis nauplii stage 5-6
* dinobryon sociale
* cyclops kolensis nauplii stage 3-4
* conochilus unicornis
* collotheca mutabilis with egg
* cyclops kolensis nauplii stage 1-2
* cyclopidae
* bosmina longispina young
* keratella cochlearis with egg
* notholca squamula
* synchaeta prominula
* harpacticella inopinata
* spirogyra
* filinia terminalis without egg
* synchaeta grandis
* epischura baikalensis nauplii stage 6
* algae
* asterionella formosa
* cyclops copepoda stage
* kellicottia longispina with egg
* polyarthra vulgaris
* kellicottia longispina without egg
* epischura baikalensis adult male
* vorticella
* epischura baikalensis nauplii stage 3
* asplanchna priodonta priodonta
* copepoda
* epischura baikalensis nauplii stage 2
* notholca intermedia without egg
* cyclops kolensis copepoda stage 5
* cyclops kolensis copepoda stage 4
* synchaeta
* epischura baikalensis copepoda stage 5
* other
* epischura baikalensis
* keratella cochlearis without egg
* bosmina longirostris young
* cladocera egg
* filinia terminalis with egg
* synchaeta pachypoda

</summary>
 -->
 
## Data format description

File `data.json` contains list of objects in images.
* Field `image` contains direct link for source image to download
* `category` contains object class
* `points` is a list of polygon coordinates; each point is represented by `dict` with `x` and `y` coordinates of point, each coordinate is in span `[0,1]` from left and top
```json
{
  "image": "https://storage.yandexcloud.net/baikal-samples/images/d30543d7-4881-4160-8c25-f014dddeffa4-New2/d07053cd-77ef-4410-8b4f-27607b24977f-21-09-14-12-57-27.jpg", 
  "category": "cyclotella minuta", 
  "points": [
    {"x": 0.3097988874625588, "y": 0.9425188988731992},
    {"x": 0.3662815575524176, "y": 0.9425188988731992}, 
    {"x": 0.3662815575524176, "y": 0.9904435886464127}, 
    {"x": 0.3097988874625588, "y": 0.9904435886464127}]}
```

## Changelog

### ver [0.0.1] - 2022-09-23
First version of dataset
