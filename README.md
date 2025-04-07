- 👋 Hi, I’m @Devil7757
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Devil7757/Devil7757 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---># Example Meep FDTD simulation setup (simplified)
import meep as mp

# Define iPhone-like antenna geometry
cell = mp.Vector3(16, 16, 0)
geometry = [mp.Cylinder(radius=0.5, material=mp.Medium(epsilon=12))]

sources = [mp.Source(mp.ContinuousSource(frequency=2.4e9),  # Wi-Fi frequency
           component=mp.Ez,
           center=mp.Vector3(0,0))]

sim = mp.Simulation(cell_size=cell,
                    geometry=geometry,
                    sources=sources,
                    resolution=10)

sim.run(until=100)

