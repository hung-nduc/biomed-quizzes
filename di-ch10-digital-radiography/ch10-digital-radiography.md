---
title: "Diagnostic Imaging, Ch. 10: Digital Radiography"
description: "A thorough check of the Chapter 10 slides: why digital, computed radiography, direct and indirect DR, image structure and quality, post-processing, PACS and DICOM. Slide numbers are given in the explanations."
id: di-ch10-digital-radiography
feedback: instant
shuffle_choices: true
pass_mark: 60
tags: [ch10]
---

# 1. Why digital? {time=10m}

Screen-film radiography versus digital radiography (slides 2 to 9).

## Which imaging modality is described as the only "non-digital" one still in everyday use? {type=single id=intro-nondigital tags=intro}

- [x] Plain radiography (X-ray on film)
- [ ] Ultrasound
- [ ] Computed tomography
- [ ] Digital subtraction angiography

::: explanation
Slide 2: ultrasound, CT, MRI and DSA already have integrated digital techniques. Plain X-rays are the last non-digital modality, so a filmless department needs plain films in digital form too.
:::

## Roughly what share of a radiology department's workload is plain radiography? {type=single id=intro-workload tags=intro}

- [ ] 10 to 20 %
- [ ] 30 to 40 %
- [x] 70 to 80 %
- [ ] Over 95 %

::: explanation
Slide 2: plain radiography is the backbone of radiology and makes up 70 to 80 % of the workload.
:::

## Select every limitation of screen-film radiography. {id=intro-film-limits type=multi points=2 tags=intro}

- [x] The radiographic speed is fixed, so the dose cannot be adjusted on the spot
- [x] Many toxic chemicals are used in processing
- [x] The repeat-exposure rate is high (up to about 20 % of examinations in some branches)
- [ ] Image quality depends mainly on the signal-to-noise ratio of the detector
- [ ] Brightness and grey scale can be changed freely after the exposure

::: explanation
Slide 5 lists a fixed speed and dose latitude, fixed brightness and grey scale, toxic chemicals, time-intensive work, high repeat rate and difficult archiving. Dependence on SNR (slide 6) belongs to digital radiography, and film brightness and grey scale cannot be adjusted.
:::

## In digital radiography, image quality depends mainly on which quantity? {type=single id=intro-snr tags=intro}

- [ ] The characteristic curve of the screen-film combination
- [x] The signal-to-noise ratio (SNR)
- [ ] The temperature of the chemical processor
- [ ] The speed class of the film

::: explanation
Slide 6: in screen-film radiology image quality is a built-in property of the film. In digital radiography it depends on SNR, so the dose can be varied to reach the SNR that is needed.
:::

## Complete the comparison. {id=intro-film-blanks type=blanks tags=intro}

In screen-film radiography the film is the acquisition, display and [[archive|archiving]] medium, and the dose is set by the screen-film [[speed]]. In digital radiography acquisition, display and archive are [[separated|separate|separate steps]], and the dose is variable.

::: explanation
Slide 6. Separating acquisition, display and archive is what allows post-processing, PACS storage and teleradiology.
:::

## Putting acquisition, display and archiving into separate steps is a key feature of digital radiography, while film does all three. {id=intro-separation type=truefalse tags=intro}

```answer
value: true
```

::: explanation
Slide 6: film is the acquisition, display and archive medium; digital radiography separates the three.
:::

## Which of these are advantages of digital imaging named in the slides? {id=intro-advantages type=multi points=2 tags=intro}

- [x] Easy data manipulation (post-processing)
- [x] Data transfer through PACS and telemedicine
- [x] Space-saving data storage
- [x] Dose reduction is strongly associated with digital radiography
- [ ] Digital radiography needs no X-ray tube
- [ ] The patient receives no radiation at all

::: explanation
Slides 7 and 8: data manipulation, transfer (PACS, telemedicine), storage, robustness, consistency, flexibility and communication, and dose reduction. The X-ray tube is still needed (slide 13).
:::

## Put the steps of the standard DR process in order. {id=intro-dr-process type=ordering points=3 tags=intro}

1. The X-ray beam is produced by a standard radiographic X-ray tube
2. The image is captured by the digital image detector
3. The signal is digitised by an analogue-to-digital converter (ADC)
4. The data are transferred to the system computer
5. The image is post-processed
6. The image is shown on a suitable display device

::: explanation
Slide 13 lists seven steps. They also include an output to video format through a digital-to-analogue converter (DAC) between transfer and post-processing, which is left out here.
:::

# 2. Computed radiography (CR) {time=20m}

Phosphor imaging plates, the reader and the readout chain (slides 16 to 36).

## Why is CR called a "two-step" process while DR is a "one-step" process? {type=single id=cr-twostep tags=cr}

- [ ] CR needs two separate x-ray exposures of the patient
- [x] CR needs a separate reader, while DR forms the image in the detector
- [ ] CR stacks two imaging plates in one cassette
- [ ] DR images are exposed on film and then scanned later

::: explanation
Slides 4 and 38: in CR the cassette is taken from under the patient and fed into a reader. In DR the image goes straight from the detector to the screen.
:::

## What does a CR cassette contain? {type=single id=cr-cassette tags=cr}

- [ ] A sheet of silver halide film between two screens
- [x] A photostimulable phosphor imaging plate
- [ ] A scintillator coupled to a CCD
- [ ] A layer of amorphous selenium

::: explanation
Slides 14 and 17: x-rays form a latent image in the phosphor screen of the cassette, and a laser reader later releases the stored signal.
:::

## Which kind of luminescence do computed radiography plates use to store the image? {type=single id=cr-luminescence tags=cr}

- [ ] Fluorescence, a prompt emission
- [x] Phosphorescence, a delayed emission
- [ ] Bremsstrahlung, braking radiation
- [ ] Cherenkov radiation, light from fast particles

::: explanation
Slide 18: fluorescence (prompt emission) predominates in screen-film radiography. Phosphorescence (delay of minutes to days, speeded by coloured light) lets energy be stored temporarily without film, which is exactly what CR exploits.
:::

## Match the type of luminescence to its description. {id=cr-lumi-match type=matching points=2 tags=cr}

- X-ray fluorescence :: Prompt emission of light, the mechanism that predominates in screen-film radiography
- X-ray phosphorescence :: Delayed emission that stored energy releases when stimulated by light, exploited in CR
- :: Emission of electrons from the anode of the tube

::: explanation
Slide 18 and the diagram on slide 19. The last option is a distractor.
:::

## What is the active material of a CR imaging plate? {type=single id=cr-material tags=cr}

- [ ] Caesium iodide doped with thallium
- [ ] Amorphous selenium
- [x] Barium fluorohalide activated with divalent europium
- [ ] Amorphous silicon doped with hydrogen

::: explanation
Slide 22: phosphor crystals of barium fluorohalide activated with divalent europium ions sit in a polymer binder. CsI:Tl and a-Si:H belong to indirect DR; a-Se to direct DR.
:::

## What does PSP stand for in "PSP plate"? {id=cr-psp type=short tags=cr}

```answer
accept:
  - photostimulable storage phosphor
  - photo-stimulable storage phosphor
  - photostimulable storage phosphors
  - photostimulable phosphor
  - photostimulable storage phosphor plate
```

::: explanation
Slide 23: photostimulable storage phosphor plates.
:::

## Which of these are layers of a standard CR imaging plate? {id=cr-layers type=multi points=2 tags=cr}

- [x] A thin protective layer
- [x] The photostimulable phosphor layer
- [x] A conduction layer
- [x] A polyester base with a reflective backing
- [ ] A CsI:Tl needle layer
- [ ] An a-Se photoconductor layer
- [ ] A TFT switching array

::: explanation
Slides 23 and 24. The CsI:Tl layer, the a-Se layer and the TFT array are parts of flat-panel DR detectors.
:::

## What is the purpose of the conduction layer in an imaging plate? {type=single id=cr-conduction tags=cr}

- [ ] It amplifies the signal before the readout
- [x] It reduces static charge and improves sharpness
- [ ] It stores the latent image
- [ ] It reflects the laser back into the phosphor

::: explanation
Slide 23. The conduction layer is not part of the signal chain: it drains static charge that would otherwise disturb the plate, and by absorbing stray light it keeps the image sharp. Storage is the phosphor's job, and the reflective layer is a separate layer.
:::

## Compared with a standard imaging plate, a high-resolution plate has which properties? {type=single id=cr-hires tags=cr}

- [ ] A thicker layer and larger crystals: sharper and more absorbing
- [x] A thinner layer and smaller crystals: sharper, but less x-ray absorption
- [ ] A reflective layer and a 40 % absorption
- [ ] The same crystals, but a thicker protective coat

::: explanation
Slide 25. The standard plate has a thicker layer, larger crystals, a light-reflection layer, general use and about 40 % fractional absorption. The high-resolution plate is thinner, has smaller crystals and no reflective layer, and absorbs less.
:::

## Put the steps of CR image acquisition and readout in order. {id=cr-steps type=ordering points=3 tags=cr}

1. X-ray exposure forms the latent image in the phosphor plate
2. A red laser scans the plate
3. The stimulated phosphor releases blue light
4. A photomultiplier tube turns the light into an electrical signal
5. An analogue-to-digital converter digitises the signal
6. Bright light erases the residual image so the plate can be reused

::: explanation
Slides 26 to 31. Erasure comes last because readout is destructive.
:::

## Complete the readout description. {id=cr-readout-blanks type=blanks points=2 tags=cr}

During readout the plate is scanned by a [[red]] laser beam. The trapped electrons relax and release [[blue]] light. [[optical fibres|optical fibers|fibre optics|light guides]] collect it and carry it to a [[photomultiplier tube|photomultiplier|PMT|PM tube]], which produces an electrical current.

::: explanation
Slide 28 (and the diagram on slide 26).
:::

## How many electrons can one absorbed x-ray photon leave trapped in the phosphor? {type=single id=cr-trapped tags=cr}

- [ ] About one
- [ ] About ten
- [x] More than 100
- [ ] Exactly as many as the photon energy in keV

::: explanation
Slide 27: the photoelectron ionises many atoms along its track, so one absorbed photon gives rise to over 100 trapped electrons.
:::

## A latent image left on an imaging plate stays unchanged indefinitely until it is read. {id=cr-decay type=truefalse tags=cr}

```answer
value: false
```

::: explanation
Slide 28: left long enough, the trapped electrons relax spontaneously and the image decays over time. Reading it soon after exposure matters.
:::

## Why is CR readout called "destructive"? {type=single id=cr-destructive tags=cr}

- [ ] The laser burns the phosphor, so the plate is discarded
- [x] It erases the latent image; bright light then clears the rest
- [ ] The cassette is opened and the film is destroyed
- [ ] The photomultiplier tube is damaged on each read

::: explanation
Slide 31. Reading the plate with the laser releases the stored energy, so the latent image is gone afterwards. A bright-light erase then clears what is left so the plate can be reused; the plate itself is not damaged, which is why the other options are wrong.
:::

## Dual-energy imaging with CR can produce separate "tissue only" and "bone only" images. {id=cr-dual type=truefalse tags=cr}

```answer
value: true
```

::: explanation
Slides 32 and 63: from a low- and a high-energy exposure, soft tissue and bone can be separated.
:::

# 3. Digital radiography (DR): indirect and direct {time=20m}

Flat-panel detectors, scintillators, photoconductors and the TFT array (slides 37 to 55).

## What is the main difference between CR and DR? {type=single id=dr-vs-cr tags=dr}

- [ ] DR reads a phosphor plate with a laser
- [x] DR needs no cassette; the detector sends the signal directly
- [ ] DR images must be developed with chemicals
- [ ] DR cannot be post-processed

::: explanation
Slides 14 and 38. CR needs a cassette that is carried to a separate reader (two steps). In DR the detector stays in the bucky and the signal goes straight to the readout electronics. Both produce digital images, so both can be post-processed, and neither uses a chemical processor.
:::

## Complete the conversion chains. {id=dr-chains type=blanks points=2 tags=dr}

Indirect DR converts X-rays to [[light|light photons|visible light]] and then to an electrical signal. Direct DR converts X-rays directly to electrical [[charge|charges]].

::: explanation
Slides 38 and 46.
:::

## Which scintillator is used in indirect flat-panel DR? {type=single id=dr-scintillator tags=dr}

- [ ] Amorphous selenium (a-Se)
- [ ] Barium fluorohalide (BaFBr:Eu)
- [x] Caesium iodide doped with thallium (CsI:Tl)
- [ ] Amorphous silicon (a-Si:H)

::: explanation
Slides 40 and 41. Indirect flat panels convert x-rays to light in CsI:Tl and then light to charge in an a-Si photodiode array. A-Se is the photoconductor of direct detectors, and barium fluorohalide is the CR phosphor.
:::

## Name the scintillator material used in indirect DR (chemical name or formula). {id=dr-scint-short type=short tags=dr}

```answer
accept:
  - CsI
  - "CsI:Tl"
  - caesium iodide
  - cesium iodide
  - caesium iodide thallium
  - cesium iodide thallium
  - caesium iodide doped with thallium
  - cesium iodide doped with thallium
```

::: explanation
Slide 41: a thin (about 500 micrometre) layer of CsI:Tl coated onto the a-Si:H array.
:::

## About how many light photons does one absorbed x-ray photon release in a CsI:Tl scintillator? {id=dr-3000 type=numeric tags=dr}

```answer
value: 3000
rel_tolerance: 0.15
```

::: explanation
Slides 40 and 41: about 3000 photons, in the green part of the spectrum.
:::

## Fill in the colours. {id=dr-colours type=fields points=3 tags=cr,dr}

```answer
fields:
  - label: "Colour of the laser that stimulates the CR plate"
    accept: ["red"]
  - label: "Colour of the light released by the stimulated CR plate"
    accept: ["blue"]
  - label: "Colour of the light released by a CsI:Tl scintillator"
    accept: ["green"]
```

::: explanation
Slides 28 and 41: red laser in, blue light out for CR; green light from CsI:Tl in indirect DR.
:::

## Why is CsI:Tl grown as a channelled (columnar) crystal structure? {type=single id=dr-channel tags=dr}

- [ ] To increase the amount of scatter
- [x] To keep the light from spreading sideways and so minimise unsharpness
- [ ] To make the layer thick enough to stop the laser
- [ ] To convert x-rays directly into charge

::: explanation
Slide 41. The needle-like columns act as light guides, so the light travels towards the photodiode instead of spreading sideways. This lets the layer be thick enough to absorb x-rays without losing sharpness. Direct conversion into charge is the job of a-Se, not CsI.
:::

## What is the "a-Si:H" active matrix made of? {type=single id=dr-asi tags=dr}

- [ ] Crystalline silicon bonded to selenium
- [x] An amorphous silicon layer doped with hydrogen
- [ ] Silver halide crystals
- [ ] Barium fluorohalide in a binder

::: explanation
Slide 42. The active matrix is hydrogenated amorphous silicon (a-Si:H), the material the photodiodes and TFT switches are built on. It is not crystalline silicon, and selenium belongs to the direct detector's photoconductor.
:::

## Name the three components that make up each pixel of the indirect-DR active matrix. {id=dr-pixel type=fields points=3 tags=dr}

```answer
fields:
  - label: "Light sensor"
    accept: ["photodiode", "a photodiode"]
  - label: "Stores the charge of the latent image"
    accept: ["charge storage capacitor", "storage capacitor", "capacitor"]
  - label: "Switch that reads the pixel out"
    accept: ["thin-film transistor", "thin film transistor", "TFT", "TFT switch", "transistor"]
```

::: explanation
Slide 42 (and slide 40 for the roles). Each TFT corresponds to one pixel (slide 43).
:::

## Complete the definition. {id=dr-fill-blanks type=blanks tags=dr}

Fill factor = [[sensitive area|sensitive|light-sensitive area]] / [[overall area|total area|pixel area|overall pixel area]].

::: explanation
Slides 40 and 42. The transistor and capacitor take up part of the pixel, and light falling there forms no image.
:::

## A pixel has an overall area of 0.04 mm² and a sensitive area of 0.03 mm². What is its fill factor? {id=dr-fill-num type=numeric tags=dr}

```answer
value: 0.75
tolerance: 0.01
```

::: explanation
Fill factor = sensitive area / overall area = 0.03 / 0.04 = 0.75 (75 %).
:::

## The pixels are made smaller to improve resolution, but the circuitry stays the same size. What happens to the fill factor and efficiency? {type=single id=dr-fill-trend tags=dr}

- [ ] Both increase
- [x] Both decrease, because the circuitry takes up a larger share of each pixel
- [ ] The fill factor is unchanged because it depends only on the scintillator
- [ ] The fill factor rises but efficiency falls

::: explanation
Slide 42. The fill factor is the sensitive share of each pixel. The circuitry (TFT, wiring) keeps a fixed size, so smaller pixels leave less area for the photodiode: fill factor and efficiency both fall. This is the trade-off between resolution and dose efficiency.
:::

## Put the steps of image formation in an indirect flat-panel detector in order. {id=dr-indirect-steps type=ordering points=3 tags=dr}

1. An x-ray photon is absorbed in the CsI:Tl scintillator
2. About 3000 green light photons are released
3. The photodiode of the a-Si:H pixel detects the light
4. The charge storage capacitor stores the latent image
5. The TFT switch reads out the pixel
6. The voltage signal is digitised

::: explanation
Slides 39 and 40.
:::

## What is the X-ray window of a flat-panel detector, and what is it for? {type=single id=dr-window tags=dr}

- [ ] A lead shutter that limits the beam size
- [x] A low-absorption cover of aluminium or carbon fibre
- [ ] A glass plate that stores the latent image
- [ ] A filter that colours the light blue

::: explanation
Slide 44. The window is a cover over the detector. It is made of material that absorbs little, so most x-ray photons reach the scintillator and less scatter is produced. It does not limit the beam, store an image or filter light.
:::

## Which photoconductor is used most commonly in direct DR? {id=dr-ase type=short tags=dr}

```answer
accept:
  - a-Se
  - a-selenium
  - amorphous selenium
  - selenium
  - amorphous Se
```

::: explanation
Slide 45: the photoconductor converts x-ray energy directly into free electrons and holes, with no light photons in between.
:::

## An a-Se photoconductor layer replaces the scintillator in direct DR. {id=dr-direct-no-scint type=truefalse tags=dr}

```answer
value: true
```

::: explanation
Slide 45: a photoconductor is used instead of a scintillator.
:::

## Put the steps of image formation in a direct (a-Se) detector in order. {id=dr-direct-steps type=ordering points=3 tags=dr}

1. The x-ray photon is absorbed in the a-Se photoconductor
2. Electrons and positive holes are created
3. A positive surface electrode attracts the electrons
4. The positive charges are drawn to the charge storage capacitor, forming the latent image
5. Rows of TFT switches are gated in turn and charge-sensitive amplifiers read the charge
6. The voltage signal is digitised and sent to the system computer

::: explanation
Slide 47. Photon absorption creates electron-hole pairs in the a-Se. The applied field sends the charges towards the electrodes, the capacitors collect them as the latent image, and the TFT rows then release the charge for amplification and digitisation. No light is involved, which is why direct detectors are sharper.
:::

## Which statements about direct DR are correct? {id=dr-direct-multi type=multi points=2 tags=dr}

- [x] No scintillator or light conversion step is involved
- [x] The latent image is held as charge in storage capacitors
- [x] A TFT array reads the charge out pixel by pixel
- [ ] The image is formed by about 3000 green light photons per x-ray photon
- [ ] A red laser scans the detector to read it

::: explanation
Slides 45 and 47. The 3000 green photons belong to CsI:Tl (indirect) and the laser to CR.
:::

## Match each material or component to its role. {id=dr-match-materials type=matching points=4 tags=cr,dr}

- Barium fluorohalide (Eu) :: Photostimulable phosphor of the CR imaging plate
- CsI:Tl :: Scintillator of indirect DR that emits green light
- a-Se :: Photoconductor of direct DR that makes charge directly
- a-Si:H :: Active matrix with a photodiode, capacitor and TFT per pixel
- :: Phosphor screen that absorbs the laser light

::: explanation
Slides 22, 41, 42 and 45. The last option is a distractor.
:::

## Which of these are listed as types of direct digital radiography on slide 55? {id=dr-direct-types type=multi points=2 tags=dr}

- [x] Flat-panel detector (FPD) systems
- [x] CCD-based systems
- [x] Slot-scanning systems
- [x] Photon-counting type
- [ ] Film digitisers
- [ ] CR plate readers

::: explanation
Slide 55. The slide lists flat-panel detectors, CCD-based systems, slot-scanning systems and photon-counting types as direct digital radiography. Film digitisers and CR plate readers still depend on film or a plate and are not direct DR.
:::

## In a CCD-based indirect system, how does the light from the scintillator reach the CCD? {type=single id=dr-ccd tags=dr}

- [ ] It is conducted by an a-Se layer
- [x] By optical coupling
- [ ] It is stored on a charge capacitor first
- [ ] By a TFT array

::: explanation
Slide 54 shows the scintillator optically coupled to a CCD, whereas flat panels use a TFT array.
:::

# 4. Digital image structure and quality {time=10m}

Pixels, bit depth, resolution and image-quality parameters (slides 33 to 36).

## How many different grey values can a pixel with 8 bits store? {id=quality-8bit type=numeric tags=quality}

```answer
value: 256
```

::: explanation
Slide 33: N bits give $2^N$ values, so $2^8 = 256$ (which equals 1 byte).
:::

## How many grey levels does a 12-bit pixel provide? {id=quality-12bit type=numeric tags=quality}

```answer
value: 4096
```

::: explanation
A pixel with n bits has $2^n$ grey levels, so $2^{12} = 4096$. Each extra bit doubles the number of levels, so 8 bits give 256 and 16 bits give 65536.
:::

## How many bits per pixel are needed to represent 1024 grey levels? {id=quality-bits type=numeric tags=quality}

```answer
value: 10
```

::: explanation
$2^{10} = 1024$. Slide 33: N bits give $2^N$ values.
:::

## What happens when the bit depth is increased? {type=single id=quality-bitdepth tags=quality}

- [ ] Fewer grey levels and a smaller file
- [x] More grey levels and a larger file
- [ ] Better spatial resolution but the same file size
- [ ] More grey levels with no change in file size

::: explanation
Slide 34: a larger bit depth increases the grey scale and the file size.
:::

## Smaller pixels generally give better spatial resolution. {id=quality-pixelsize type=truefalse tags=quality}

```answer
value: true
```

::: explanation
Slide 34: the smaller the pixel, the better the resolution.
:::

## Match each system to its typical pixel size. {id=quality-pixelmatch type=matching points=3 tags=quality}

- CR :: 50 to 200 micrometres
- DR :: 100 to 200 micrometres
- Digital mammography :: 50 to 100 micrometres
- :: 500 to 1000 micrometres

::: explanation
Slide 34. The last option is a distractor.
:::

## In which unit is spatial resolution expressed? {id=quality-lpmm type=short tags=quality}

```answer
accept:
  - lp/mm
  - "line pairs/mm"
  - line pairs per mm
  - line pairs per millimetre
  - line pairs per millimeter
  - lp per mm
```

::: explanation
Slide 35: spatial resolution (fine detail) is expressed in lp/mm and depends on the sampling frequency and the number of pixels.
:::

## Which are listed as image-quality parameters for CR imaging? {id=quality-params type=multi points=2 tags=quality}

- [x] Speed
- [x] Latitude (dynamic range)
- [x] Spatial resolution and the modulation transfer function (MTF)
- [x] Detective quantum efficiency (DQE)
- [ ] Temperature of the developer
- [ ] Number of rinse cycles

::: explanation
Slide 36. Speed, latitude, spatial resolution (MTF) and DQE are the quality measures the slides use for CR. Developer temperature and rinse cycles belong to wet film processing, which CR does not use.
:::

## Match each abbreviation to its meaning. {id=quality-abbrev type=matching points=5 tags=quality,pacs}

- ADC :: Analogue-to-digital converter
- TFT :: Thin-film transistor
- LUT :: Look-up table
- MTF :: Modulation transfer function
- DQE :: Detective quantum efficiency
- :: Digital quality evaluation

::: explanation
Slides 13, 36, 42 and 51. The last option is a distractor.
:::

# 5. Post-processing and display {time=15m}

Artefacts, calibration, auto-ranging, enhancement and monitors (slides 48 to 68).

## What causes irregular shading across the field of a digital image? {type=single id=post-shading tags=post}

- [ ] A laser that is out of focus on the plate
- [x] Uneven sensitivity or gain of the absorption layer
- [ ] A defective TFT row in the matrix
- [ ] Too high a bit depth

::: explanation
Slide 49. Shading is a smooth, uneven brightness caused by gain or sensitivity differences over the absorption layer, and it is corrected with a gain (flat-field) map. A defective TFT row would give a line, not a gradual shading, and bit depth does not cause it.
:::

## What typically causes bright or dark spots or lines in the image? {type=single id=post-lines tags=post}

- [ ] Gain variation of the scintillator layer
- [x] Defective pixels, rows or columns in the active matrix
- [ ] Too narrow a histogram
- [ ] Hardcopy printing

::: explanation
Slide 49. Isolated bright or dark spots, lines or bands come from individual dead pixels or whole rows and columns of the active matrix, which are corrected by interpolating from neighbours. Gain variation gives smooth shading instead.
:::

## Match each problem or technique to the correction or purpose. {id=post-match type=matching points=4 tags=post}

- Irregular shading across the field :: Gain calibration with a uniform-exposure mask image
- Defective pixels in the array :: Pixel calibration by interpolating working neighbouring pixels
- Remapping grey values to a new range :: Look-up table (LUT)
- Excluding unneeded very high and very low data values :: Histogram analysis in auto-ranging
- :: Raising the tube kilovoltage

::: explanation
Slides 49 to 51. The last option is a distractor.
:::

## Put the steps of auto-ranging in order. {id=post-autorange type=ordering points=2 tags=post}

1. Identify the relevant image field
2. Generate a histogram of the number of pixels at each grey value
3. Analyse the histogram and exclude ranges with no clinical information
4. Normalise the selected grey-scale range to the display

::: explanation
Slide 50. The system first finds the image field, then builds the histogram, removes ranges without clinical information (for example air or collimator edge) and finally maps the remaining range to the display. The histogram has to exist before it can be analysed.
:::

## Shifting the gradient and position of the look-up table changes which image property? {type=single id=post-lut tags=post}

- [ ] The pixel size
- [x] The mean brightness and the displayed contrast
- [ ] The number of bits per pixel
- [ ] The dose to the patient

::: explanation
Slide 51. The look-up table maps stored values to displayed grey levels. Its gradient sets the contrast and its position sets the brightness. It changes only the display, not the pixel size, bit depth or patient dose.
:::

## Put the steps of unsharp-mask spatial enhancement in order. {id=post-unsharp type=ordering points=2 tags=post}

1. Produce a blurred version of the original image
2. Subtract the blurred image from the original to keep only the fine detail
3. Add the fine-detail image back onto the original
4. The result is an enhanced composite image

::: explanation
Slide 52. Unsharp masking gives edge enhancement (slide 57).
:::

## Which are advantages of flat-panel (liquid-crystal) monitors over CRT displays, according to the slides? {id=post-monitor type=multi points=2 tags=post}

- [x] Higher contrast
- [x] Greater resolution
- [x] Lower power use
- [ ] They need an evacuated glass tube
- [ ] They scan a phosphor screen with an electron beam

::: explanation
Slide 53. The last two describe the CRT.
:::

## Match each kind of image processing to its effect. {id=post-tonefreq type=matching points=2 tags=post}

- Tone processing :: Sets density and contrast by changing the characteristic curve
- Frequency processing :: Controls the sharpness of objects in the image
- :: Reduces the patient dose after exposure

::: explanation
Slide 57. The last option is a distractor: processing cannot lower the dose after the exposure has been made.
:::

## Why is DR well suited to mammography? {type=single id=post-mammo tags=post}

- [ ] It always needs a higher dose than film
- [x] Wide latitude for dense and fatty breasts, with contrast for small masses
- [ ] It removes the need for breast compression
- [ ] It records only high-energy photons

::: explanation
Slide 59. DR gives a wide latitude, so dense and fatty tissue are both shown, and enough contrast to see small masses and microcalcifications. It does not remove compression and it is not limited to high-energy photons.
:::

## Which are benefits of DR in gastrointestinal imaging listed in the slides? {id=post-gi type=multi points=2 tags=post}

- [x] Faster acquisition with instant display and post-processing
- [x] Reduced motion blur
- [x] Fewer re-exposures
- [x] Shorter downtime between exposures
- [ ] A fixed grey scale that cannot be adjusted

::: explanation
Slide 61. DR displays the image almost at once and can be post-processed, shortens exposures and so reduces motion blur, avoids repeats and cuts the time between exposures. The grey scale can be adjusted, so the last option is wrong.
:::

## Tomosynthesis needs the detector to move during the exposure. {id=post-tomo type=truefalse tags=post}

```answer
value: false
```

::: explanation
Slide 64: like tomography, but the detector does not move; pixels are shifted and added.
:::

## What does dual-energy imaging make possible? {type=single id=post-dual tags=post}

- [ ] Imaging two patients at once
- [x] Separating soft tissue from bone
- [ ] Doubling the pixel count
- [ ] Printing on two film sizes

::: explanation
Slide 63. Two exposures at different energies exploit the different energy dependence of bone and soft tissue, so one can be subtracted to show the other. It does not double the pixel count or the number of patients.
:::

## A mobile DR system typically uses a detector of about what size, connected to the mobile x-ray unit by a cable? {type=single id=post-mobile tags=post}

- [ ] 5 x 7 inches
- [ ] 10 x 12 inches
- [x] 17 x 14 inches
- [ ] 36 x 36 inches

::: explanation
Slide 63. Mobile DR uses a portable detector of about 17 x 14 inches, similar in size to a large cassette, connected to the mobile x-ray unit by a cable. The smaller sizes are too small for chest work and 36 x 36 inches is a fixed room detector.
:::

# 6. PACS and DICOM {time=5m}

Archiving and communication (slide 69).

## What does a PACS aim to do? {type=single id=pacs-aim tags=pacs}

- [ ] Produce x-rays at a higher tube voltage to cut patient dose
- [x] Replace film and paper records with an electronic network and monitor viewing
- [ ] Digitise old film with a laser scanner for archiving
- [ ] Erase imaging plates with bright light after reading

::: explanation
Slide 69. A PACS replaces film, paper request forms and written reports with an electronic network, so images appear on monitors together with the clinical details and the report. The other options describe x-ray generation, film digitisation and plate erasure, which are different things.
:::

## What is DICOM? {type=single id=pacs-dicom tags=pacs}

- [ ] A brand of flat-panel detector sold for radiography
- [x] A standard for storing, printing and transmitting medical images
- [ ] A type of photoconductor layer used in detectors
- [ ] A display technology for diagnostic monitors

::: explanation
Slide 69. It lets scanners, servers, workstations, printers and network hardware from many makers work together in a PACS.
:::

## DICOM conformance statements state which DICOM classes a device supports. {id=pacs-conformance type=truefalse tags=pacs}

```answer
value: true
```

::: explanation
Slide 69. A conformance statement is the manufacturer's document that lists which DICOM classes (such as storage or print) a device supports, so buyers can check that two devices will work together.
:::

## Spell out the abbreviations: what do the letters PACS stand for? {id=pacs-spell type=short tags=pacs}

```answer
accept:
  - picture archiving and communication system
  - picture archiving and communications system
  - picture archiving & communication system
```

::: explanation
Slide 69. PACS stands for picture archiving and communication system. The accepted spellings include the plural 'communications' and the ampersand form.
:::

# 7. Written answers {time=15m}

These are graded by an AI reviewer from the rubric after you export your answers.

## Compare computed radiography with indirect and direct digital radiography. {id=essay-compare type=essay points=8 tags=cr,dr}

Describe how each system captures and reads out the image, and give one practical advantage of DR over CR.

```answer
min_words: 120
max_words: 400
rubric:
  - "CR: states that a phosphor plate stores a latent image (phosphorescence), is read by a red laser, releases blue light that a photomultiplier tube converts, and is erased for reuse"
  - "Indirect DR: names the scintillator (CsI:Tl), light photons, and the a-Si:H pixel with photodiode, storage capacitor and TFT"
  - "Direct DR: names the photoconductor (a-Se), electron-hole pairs, charge storage and TFT readout without a light step"
  - "Gives a correct practical advantage of DR over CR (no cassette handling, immediate image)"
  - "Clear structure and correct terminology"
sample_answer: |
  In CR, x-rays are absorbed in a photostimulable phosphor plate (barium fluorohalide with europium) in a cassette, which stores a latent image by phosphorescence. The cassette is taken to a reader, where a red laser stimulates the plate. The plate releases blue light, collected by optical fibres onto a photomultiplier tube; the signal is digitised by an ADC, and bright light then erases the plate for reuse.

  In indirect DR a CsI:Tl scintillator turns each x-ray photon into about 3000 green light photons. The photodiode of each a-Si:H pixel detects the light, a storage capacitor holds the charge and a TFT switch reads it out. In direct DR an a-Se photoconductor converts x-rays straight into electrons and holes; the holes are collected in the storage capacitor and read out by TFTs, with no light step.

  DR needs no cassette handling, so the image appears at once and the workflow is faster.
```

## Explain why digital radiography can allow a variable dose, and what the radiologist must watch for. {id=essay-dose type=essay points=6 tags=intro,quality}

Refer to image quality, SNR and the way film works.

```answer
min_words: 80
max_words: 300
rubric:
  - "Explains that film has a fixed speed and latitude, so the dose is set by the screen-film combination"
  - "Explains that digital image quality depends on SNR, so the dose can be chosen to reach the required SNR"
  - "Mentions that post-processing (window, LUT, auto-ranging) can adjust brightness and contrast after exposure"
  - "States a sensible caution, such as keeping the dose high enough for adequate SNR"
```

# 8. Quick recall {time=5m}

## Complete the numbers and names. {id=recall-blanks type=blanks points=4 tags=quality,dr}

One byte is [[=8]] bits and gives [[=256]] grey values. The CsI:Tl scintillator layer is about [[=500]] micrometres thick, and a CsI:Tl layer coated on the [[a-Si:H|amorphous silicon]] array releases about [[=3000±100]] light photons per x-ray photon.

::: explanation
Slides 33 and 40 to 42.
:::
