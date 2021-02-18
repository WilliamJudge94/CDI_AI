Defect Analysis of 2-Dimensional Coherent Diffraction Imaging Data Enabled By Machine Learning
===============================================================================================

This repository is to layout all nessesary data and analysis steps to recreate a workign neural network
for this purpose.


Motivation & Features
---------------------

Raw Diffraction Data & Test Data
--------------------------------
Due to GitHub's file size limitations, please download the raw simulated diffraction patterns as well as the test data from Mendeley (link coming soon)

Data Creation
-------------

Please see https://crystal-simulation.readthedocs.io/en/latest/index.html for a detailed guide on how to - 

1) Create simulated crystals
2) Add defects for simulated crystals
3) Create 3-Dimensional CDI patterns of crystals through the use of PYNX.


File Manifest
--------------

raw_data (found at http://dx.doi.org/10.17632/2r86xtvhdz.1)
    reflection - the reflection being simulated
        sampling_rate - the sampling rate being applied to the simulation
            tif - holds the raw 3D CDI images for each type of crystal
            png - visual representation of all cdi data for each crystal

testing_data (found at http://dx.doi.org/10.17632/2r86xtvhdz.1)
    - the data and labels used for testing. 
    - Each crystal has an defect free, edge defect, and screw defect crystal inside the dataset. Created from crystals 2, 3 and 14.

trained_model-AutoKeras
    -  containes the trained AutoKeras model
    -  the base model created by AutoKeras. Must use Tensorflow 2.1.0 to import.
    
    
trained_model-VGG16
    containes the trained VGG16 model
    
trained_model-Handmade
    containes the trained Handmade model


ipynb - contains jupyter notebook files that detail how to go from raw PYNX data to the training the final neural
network model. 


Computer Requirements
---------------------

RAM - 128GB for full dataset, 64GB for trunkated dataset

GPU - 16GB of VRAM


License
-------

This project is released under the `GNU General Public License version 3`_.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

.. _GNU General Public License version 3: https://www.gnu.org/licenses/gpl-3.0.en.html
