# DVSA.MOT.SDK

A simple SDK for access to the [DVSA MOT history API](https://dvsa.github.io/mot-history-api-documentation/)

### Installation

To be able to use this SDK, you will require an Api Key, which you can apply for from the [DVSA](https://www.smartsurvey.co.uk/s/MOT_History_TradeAPI_Access_and_Support?).

DVSA.MOT.SDK is available from [NuGet](#) or as a manual download directly from GitHub.

## Usage

You will need to add the following key to your `appsettings.json` or `secrets.json`:

      {
        "MotApi": {
          "DVSAApiKey": "YOUR KEY HERE"
        }
      }
     
Then you will then need to register the apikey and SDK in your `Startup.cs` file

      services.Configure<ApiKey>(Configuration.GetSection("MotApi"));
      services.AddDvlaMotSdk();


### Contribution guidelines

To raise a new bug, create an issue on the GitHub repository. To fix a bug or add new features, fork the repository and send a pull request with your changes. Feel free to add ideas to the repository's issues list if you would to discuss anything related to the package.

## License

Copyright &copy; 2020 [Aaron Sadler](https://aaronsadler.uk/).

Licensed under the [MIT License](https://opensource.org/licenses/MIT).

The DVSA API is Licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)
