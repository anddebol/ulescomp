### Idealized urban configurations
The preliminary setup follows JAS paper [1](https://journals.ametsoc.org/view/journals/atsc/80/1/JAS-D-22-0044.1.xml)
here is a scheme for the experiments
![image](assets/images/scheme.png)


- Domain: `length = 256 m, width = 128 m,  height = 64.0 m; `
- Grid: `nx = 512; ny = 256; nz = 128`, so that uniform resolution of 0.5m in any direction is achieved
- Flow configuration: Open Channel flow with constant external pressure gradient of `dpdx =  - phys.rho_ref * ustar_r^2 /(height - buildings_height)`, where `phys.rho_ref = 1.25 kg/m^3` is reference air density, `ustar_roof = 0.25` is target dynamic velocity just above the building roofs .
- Other fluid characteristics:
```
        f = 0.0;                                # coriolis frequency [1/s]

        nu = 1.25 * 0.00001;                    # kinematic viscosity [m^2/s]
        xi = (1.0 / 0.7) * nu;                  # thermal diffusivity [m^2/s]

        rho_ref = 1.25;                         # reference density of air [kg/m^3]

        g = 9.81;                               # gravitational acceleration [m/s^2]
        Theta_ref = 283.15;                     # reference temperature [K]

        # --- no buoyancy
        beta = 0.0;                             # = g * thermal expansion coefficient = g / Theta_ref [m/(K*s^2)]
```
- Integration model time: 2hours
- Buildings setup: surface dynamic and thermal roughness parameters `z0m = 0.01 m`, `z0h = z0m/10.0`. `building_height = 16 m`. 
- Building configuration: SRF1
```
h = 16 # [m], building height
        patch_1 {
                type = "box";

                xmin = 0.0; xmax = h;   # patch dimensions
                ymin =  0.0; ymax = h;
                height = h;

                xperiod = 8.0 * h;                      #  periodicity in -x
                yperiod = 4.0 * h;                      #  periodicity in -y
        }
        patch_2 {
                type = "box";                   # patch type: "box" || "hill"

                xmin = 4.0 * h ; xmax = 5.0 * h;   # patch dimensions
                ymin =  2.0 * h; ymax = 3.0 * h;
                height = h;

                xperiod = 8.0 * h;                  # periodicity in -x
                yperiod = 4.0 * h;                  # periodicity in -y
        }
```
