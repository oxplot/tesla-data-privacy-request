**This repository is not in any way promoted by or affiliated with Tesla.**

Tesla provides data associated with your account and your vehicle upon
request. This is done via their [contact
form](https://www.tesla.com/contactus), by choosing the "Data Privacy
Request" and "Obtain a Copy of My Data" options. As of April 2022, it
may take them up to 30 days to complete the request. My request took
less than 12 hours to complete. Tesla provides more details on their
[privacy page](https://www.tesla.com/support/privacy).

This repository documents the structure of the data provided by Tesla
(as of April 2022). The findings here are based on a single request for
a single car (**Model 3 2020 Australia**). Tesla may provide more, less
or different data to different customers and for different vehicle
types. I opted to share my data with Tesla since I purchased the car.
This is an option that may be enabled in the car via the Software menu.

Depending on contributions from other Tesla owners, more vehicles may be
included in the future. If you own a Tesla and feel like contributing,
please open an issue on this repo to get started.

## Organization

[`schema`](schema) directory contains the metadata derived from content
of data provided by Tesla. This is by no means complete. Please note the
following before consuming the schema:

- `go_format` field in the schema refers to how [Golang's date
  formatting is defined](https://pkg.go.dev/time#pkg-constants).
- Value for some `enum`s are a guess based on values that were
  available.
- `optional` fields are guessed based on data.
- My car is made for the left hand drive markets (ie the driver seat is
  on the right side of the vehicle).
- `SNA` enum used in various vehicle data fields potentially means
  "Status Not Available".

[`example`](example) directory contains the data I received for my
vehicle from which the `schema` is derived. I have annonymized the
content and changed some around to preserve privacy.

The dates in the [`example/Vehicle Data`](<example/Vehicle Data>)
directory correspond to longer road trips I've been on since I bought
the car in 2020. Looks like that's what Tesla is most interested in.
