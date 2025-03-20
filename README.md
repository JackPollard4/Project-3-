# Project-3-
Project 3 Eep153

import folium

# Define a dictionary with country names and their approximate latitude and longitude
country_coords = {
    "Uganda": [1.3733, 32.2903],
    "Tanzania": [-6.3690, 34.8888],
    "Serbia": [44.0165, 21.0059],
    "Senegal": [14.4974, -14.4524],
    "Panama": [8.5380, -80.7821],
    "Nigeria": [9.0820, 8.6753],
    "Mali": [17.5707, -3.9962],
    "Malawi": [-13.2543, 34.3015],
    "Guatemala": [15.7835, -90.2308],
    "Ghana": [7.9465, -1.0232],
    "Ethiopia": [9.1450, 40.4897]
}

# Create a map centered around Africa for better visibility
map_center = [10, 10]  
world_map = folium.Map(location=map_center, zoom_start=3)

# Add markers for each country
for country, coords in country_coords.items():
    folium.Marker(
        location=coords,
        popup=country,
        icon=folium.Icon(color="red", icon="info-sign")
    ).add_to(world_map)

# Display the map
world_map



# Add USA coordinates to the dictionary
country_coords["USA"] = [37.0902, -95.7129]  # Approximate center of the USA

# Create a new map centered around Africa for better visibility
map_center = [10, 10]
world_map = folium.Map(location=map_center, zoom_start=3)

# Add markers for each country
for country, coords in country_coords.items():
    folium.Marker(
        location=coords,
        popup=country,
        icon=folium.Icon(color="red", icon="info-sign")
    ).add_to(world_map)

# Display the updated map
world_map