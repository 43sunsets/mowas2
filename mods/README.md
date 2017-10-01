# Men of War: Assault Squad 2 - modding notes

## Matrix34

NOTE: if you don't need any scaling or rotation, you can use Position instead, e.g.
`{Position -7.59774	2.36604	0.0669361}`


### 1st row:

Seems to be scaling/size. Leave this alone for the most part.

### 2nd row:

Same as above.

### 3rd row:



### 4th row:
1st number: distance from gunner/commander (Y axis)
2nd number: left/right position (X axis)
3rd number: height (Z axis)

foresight is optional, this seems to be the point where the bullets come out of?

In the SAS jeep example, {VolumeView "turret.ply"}	 is the turret pole stand for the mgun
And {VolumeView "gun_rot.ply"} is the AA crosshair gunsight on top			


			{bone "commander"
				{Matrix34
					0.707105	0.707105	-0.00227676
					-0.707107	0.707107	0
					0.00160998	0.00160998	0.999997
					-5.58237	-7.60045	1.79904
				}
			}
			{bone "driver"
				{Matrix34
					0	-0.999979	0.00644986
					1	0	0
					0	0.0064498	0.999979
					-5.94979	8.30703	2.08006
				}
			}


			{bone revolute "mgun2_rot"
				{limits -60 60}
				{Matrix34
					0	-1	0
					1	0	0
					0	0	1
					6.56786	-11.1756	8.91743
				}
				{bone revolute "mgun2"
					{limits -10 15}
					{Matrix34
						0	1	0
						0	0	1
						1	0	0
						0.0526709	-2.84459	1.7744
					}
				}
			}			
