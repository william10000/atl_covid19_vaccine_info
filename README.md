Overview

- See responses directory for sample responses

CVS

- URL: GET https://www.cvs.com/immunizations/covid-19-vaccine.vaccine-status.GA.json?vaccineinfo=
- Notes
  - Need to try out in Postman and figure out what info is needed to make the request

Kroger

- URL: GET https://www.kroger.com/rx/api/anonymous/scheduler/slots/locationsearch/pharmacy/atlanta,%20ga/2021-03-08/2021-03-30/500?appointmentReason=122&appointmentReason=125&appointmentReason=129
- Notes:
  - Not sure what 500 means
  - Returns 500 if date range is too big
  - Location can be city or zipcode
  - If you make too many requests from the browser, it requests a captcha response
  - Single request to the same URL can get responses from multiple locations

Publix

- Website: https://www.publix.com/covid-vaccine/georgia/
- API with data?: https://www.publix.com/covid-vaccine/georgia/georgia-county-status.txt?t=1615174639232
- Notes:
  - Not sure what what _t_ parameter does - looks like millisecond unix time, but the response appears to be plain text that doesn't match what the web page shows

Sams Club

- need to make account b/f looking at eligibility info

Walgreens

- URL: POST https://www.walgreens.com/hcschedulersvc/svc/v1/immunizationLocations/availability
- Request payload:
  - {"serviceId":"99","position":{"latitude":33.7489954,"longitude":-84.3879824},"appointmentAvailability":{"startDateTime":"2021-03-08"},"radius":25}

Walmart

- URL: POST https://www.walmart.com/pharmacy/v2/clinical-services/time-slots/f4abaf1c-ae0d-4c02-ad9b-c94ae881c07d
- Request payload:
  - {"startDate":"03072021","endDate":"03132021","imzStoreNumber":{"USStoreId":3710}}
  - {"startDate":"03072021","endDate":"03132021","imzStoreNumber":{"USStoreId":3775}}
- Notes:
  - Probably need multiple calls to the API to get info for each store of interest

Young Life Pharmacy

- https://form.jotform.com/210524045029142 will let you submit a partially filled out form

Clayton County: https://www.claytoncountypublichealth.org/
Cobb/Douglas County: https://www.cobbanddouglaspublichealth.com/covid-vaccine-appointments/
DeKalb County: https://www.dekalbhealth.net/covid-19-vaccine/
Fulton County: https://fultoncountyga.gov/covidvaccine
