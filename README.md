# Scanning-Helium-Microscope-Diffraction-Measuement-Simulation

Created by **Ke Wang** with help from **Boyao Liu** and **Min Lin**.

It is an interactive script that simulates the diffraction measurement of the SHeM. It allows different surface lattice structures and different pinhole plate geometry to be simulated. The input of the Multiscat is also implemented, which makes it a good script to visualize the multiscat result.

![simulation parameters](https://github.com/user-attachments/assets/2178b8f7-2d89-4f39-9471-601a7467eab1)

**Diffraction channel**: Number of diffraction channels in the script. (10 means the diffraction channels from [-10,-10] [-10,-9]... to ...[9,10] [10,10] will be examined)

**Lattice constant**: The real space lattice separation.

**Lattice vector**: Lattice vector of the unit cell.

**Beam Energy**: The simulation assumes the Helium beam is monochromatic.

**In-plane & Out-plane axis**: The full length of two axes of the elliptical detector aperture.

**Pinhole-Detector Separation**: The vertical distance between the center of the pinhole aperture and detector aperture.

**Sample z position**: The location of the sample.

![Ashem_scheme](https://github.com/user-attachments/assets/1cd7306a-ef88-406e-b09f-a9432473e9a3)

**Height Difference**: The height of the pinhole conic structure minus the height of the detector aperture conic structure. $H_p - H_d$.

**Detector tiltness**: The angle of the inclination of the detector aperture. $\beta$ in the figure above.

**Incident angle theta**: The incident polar angle of the helium beam.

**Incident angle phi**: The incident azimuthal angle of the helium beam. (currently not working)

**Lattice orientation**: To simulate the rotation of the sample or different crystal orientations in polycrystalline samples.

**reverse_latt_orientation_for_simulation**: The Multiscat changes the incident helium beam azimuthal angle, and the simulation script changes the lattice orientation. One is clockwise and the other anticlockwise, usually a reverse operation is needed if Multiscat is imported.

**Meshgrid resolution**: The number of pixels in the mesh grid script, default=1000.

**Kx, Ky mesh range**: The minimum and maximum of the $\Delta K$ displayed in the figure.

**Peak width**: The standard deviation of the Normal Distribution that gives width to each diffraction peak.

**use_reduce_in_signal_along_z**: A Normal Distribution centered at $\Delta K=0$ and multiplied to diffraction peaks to simulate the loss in signal when the sample stage moves away from specular point in real experiments.

**Pattern width**: The standard deviation of the Normal Distribution used in "use_reduce_in_signal_along_z".

**use_bg_diffuse_signal**: A Normal Distribution centered at $\Delta K=0$ and added to diffraction peaks to simulate the background diffuse noise.

**Diffuse BG width**: The standard deviation of the Normal Distribution used in "use_bg_diffuse_signal".

**Diffuse BG scale**: A coefficient that is multiplied to the Normal Distribution used in "use_bg_diffuse_signal" to control the intensity of the background noise.

**use_multiscat**: Import multiscat datafile and assign diffraction channel intensites accordingly.

**Angle step in Multiscat**: The step of change in incident helium beam azimuthal angle produced by the Multiscat, usually 2.5 or 1 degree.

**Angle compensation**: Sometimes a difference in the lattice vector interpreted from the same unit cell used in the script and Multiscat may need a compensation.

**line_plot**: The simulated line scan, turn off for better performance in generating the K space figure.

**plot_detector_path**: The detection window for a certain $Z$ range of the detector aperture projected to the $K$ space.

**z_range**: The range of $Z$ used in the "line_plot" and "plot_detector_path".

**z range linsapce**: The resolution of the z_range, higher for a smooth line, lower for better performance.

**return_line_result**: Show the x and y values in the "line_plot".

**save_plots**: Click to save the plot, but keep it turned off when adjusting parameters.

**save_plots_index**: Name of the picture file saved in "save_plots".

For plotting the 2D diffraction measurement, there is an example in the Notebook.

o(*￣▽￣*)ブ
