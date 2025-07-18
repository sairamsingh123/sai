# Daylight Factor (%) = (Ei / Eo) × 100
# Ei = Indoor illuminance (lux), Eo = Outdoor illuminance (lux)

def calculate_daylight_factor(indoor_lux, outdoor_lux):
    if outdoor_lux == 0:
        return 0
    df = (indoor_lux / outdoor_lux) * 100
    return round(df, 2)

# Example values
Ei = 150  # indoor lux
Eo = 10000  # outdoor lux (cloudy day)

df = calculate_daylight_factor(Ei, Eo)
print(f"Daylight Factor: {df} %")
