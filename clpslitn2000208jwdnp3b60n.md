---
title: "Restricting access to the website to certain sanctioned countries"
datePublished: Tue Dec 05 2023 17:10:07 GMT+0000 (Coordinated Universal Time)
cuid: clpslitn2000208jwdnp3b60n
slug: restricting-access-to-the-website-to-certain-sanctioned-countries
tags: blockchain, ipfs, sanctions

---

Often, in my projects, there is a need to somehow block access to some parts of the application to people connected from certain sanctioned or otherwise restricted jurisdictions. Doing it on the front end is usually not the best approach, but often, for blockchain projects that do not have any backend components, that might be the only option. Below is a small snippet of the code of how we did it using external APIs. This code can even run on a website powered by IPFS, i.e., without any single backend/server in your infrastructure.

```javascript
const blockedCountries = [
  { code: "VG", name: "British Virgin Islands" },
  { code: "PA", name: "Panama" },
  { code: "BY", name: "Belarus" },
  { code: "CU", name: "Cuba" },
  { code: "IR", name: "Iran" },
  { code: "IQ", name: "Iraq" },
  { code: "CI", name: "Côte d'Ivoire" },
  { code: "LR", name: "Liberia" },
  { code: "KP", name: "North Korea" },
  { code: "SD", name: "Sudan" },
  { code: "SY", name: "Syria" },
  { code: "ZW", name: "Zimbabwe" },
];

export const isCountryBlocked = async () => {
  try {
    // Get the user's IP address
    const ipResponse = await axios.get("https://api.ipify.org/?format=json");
    const ipAddress = ipResponse.data.ip;

    // Get the user's country
    const locationResponse = await axios.get(`https://api.iplocation.net/?cmd=ip-country&ip=${ ipAddress }`);
    const countryCode = locationResponse.data.country_code2;

    // Check if the country is blocked
    const blockedCountry = blockedCountries.find((country) => country.code === countryCode);
    return blockedCountry !== undefined;
  } catch (error) {
    notify(error);
    return false; // Assume country is not blocked if there's an error
  }
};
```