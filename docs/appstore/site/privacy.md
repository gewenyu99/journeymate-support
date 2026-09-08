# JourneyMate privacy policy

This policy describes JourneyMate releases with product analytics enabled and configurable crash reporting.

Effective date: **September 7, 2026**
Operator: **Vincent Ge**
Privacy contact: **[vge2606@gmail.com](mailto:vge2606@gmail.com)**

JourneyMate is an experimental travel information app. It does not require a
JourneyMate account. Preferences are stored locally, while maps, place search,
weather, official advisories, product analytics, and crash reporting when enabled use online services as described below.

## Information stored on your device

JourneyMate stores your selected country, home nationality, travel mode,
location preference, welcome-flow status, and related app preferences using local
storage. It also stores source-fetch timestamps, any reference data you choose
to download, and update-attempt/download timestamps, and may use system network
caches. The analytics SDK stores installation/session identifiers and queued events locally before transmission; crash reports may also be stored when that collection is enabled. This version does not provide an account or cloud preference sync.

You can change your choices in Settings. Deleting the app removes its local app
data; device backups and any information you shared outside the app are managed
separately by the relevant service.

## Optional reference data updates

The app includes reference numbers, embassy details, and phrases that can be
read offline. If an update source is configured, choosing **Pull latest** in
Settings requests a shared static reference-data package from that host. This
is an explicit download, not a background update or an upload of your travel
preferences or local reference cache. No JourneyMate account is required.

The configured host receives ordinary request and network metadata, such as
your IP address, request time, requested URL, and request headers. That host
may retain access logs under its own policies. Builds without a configured
update source make no reference-download request.

The app validates an update before saving it locally. Saved reference data
remains available offline; an unavailable source or failed update leaves the
existing reference data in place. If the build has no configured update source,
Pull latest reports that downloads are unavailable and makes no update request.
Content dates and source details are shown separately from device download and
attempt times; downloading data does not independently verify its contents.

## Website hosting and support email

The support and privacy website is hosted on GitHub Pages. GitHub records
visitors' IP addresses for security, including visits made without signing in.
Reference packages downloaded from this site are also served by GitHub, which
processes the associated request metadata under its policies. These pages do not add analytics, advertising, cookies, forms or tracking scripts.
See [GitHub Pages data handling](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
and [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

Support email is handled through Gmail. When you email the published address,
Google processes and stores the message and related information as the email
provider under [Google's privacy policy](https://policies.google.com/privacy).
The operator receives the details and attachments you choose to send. You can
request deletion of that correspondence using the same address.

## Location and online features

Location access is optional. You may pick a country manually instead. With your
permission, JourneyMate requests your location while you use the app. It does
not request background location or continuously record your movements.

Coordinates may be sent to Apple's location/geocoding, Maps, and WeatherKit
services to resolve a place, search nearby, display maps, or fetch weather
information. Map searches can include a geographic region and service category.
Opening directions sends the selected destination to Apple Maps. These are
online requests, so it would be inaccurate to say your position never leaves
your device. Apple's processing is governed by its own privacy terms.

For travel advisories, JourneyMate can request public information from the U.S.
Department of State, GOV.UK, or the Government of Canada. A destination can
appear in the request URL, and the provider receives ordinary network
information such as your IP address.
Selecting an official source link opens that provider's website. Network and
website providers apply their own processing and retention policies.

## Analytics and diagnostics

JourneyMate sends its existing feature-use events to PostHog Cloud in the
United States at `https://us.i.posthog.com`. Usage collection starts when this
release launches. We use this information to understand which parts of
JourneyMate are used and improve the app.

The app also includes automatic crash-reporting capability. It requires the
PostHog project's crash-autocapture setting to be enabled. That project setting
is currently off, so automatic crash collection is inactive while usage
analytics remains enabled. If crash collection is enabled, we use those reports
to investigate crashes and technical problems, as described below.

Feature-use events record actions such as opening Quick info, choosing a tool
or service category, opening a telephone prompt, viewing or playing a bundled
phrase, and opening directions. Event properties can include the selected
service/category or phrase identifier and whether location was chosen or used.
They do not include the selected telephone number, precise coordinates, home
nationality, or text you enter. The app also sends technical context such as
app and operating-system versions, device model, screen dimensions, language,
time zone, and network type.

The SDK assigns a random installation identifier and session identifiers, which
can link events and diagnostics from the same installation. These identifiers
are not your name or email, but the records are not fully anonymous. JourneyMate
has no account login and does not create PostHog person profiles or join these
records to your support email. When crash collection is enabled, reports include
technical exception types, stack traces, and diagnostic context; crash free-text
messages and recent-action breadcrumbs are removed before transmission. Those
reports may be queued on the device and sent later, including after the next
launch.

Session replay, automatic screen and interaction recording, automatic lifecycle
events, surveys, push-notification capture, and feature-flag event capture are
disabled. The app requests that PostHog disable IP-based location enrichment for
each event. PostHog still receives ordinary network metadata when handling the
request; disabling enrichment does not mean the network request has no IP
address. JourneyMate does not use these records for advertising, share them
with data brokers, or record your screen, microphone, or calls.

Analytics and diagnostic records are stored in the operator's PostHog project
under the project's and service's retention settings. This release has no
in-app analytics switch. Stopping use of or removing the app stops future app
collection; it does not erase records already received. Contact
[vge2606@gmail.com](mailto:vge2606@gmail.com) about access or deletion. Because
records use installation identifiers rather than account details, locating
particular records may require information identifying that installation.
See [PostHog's privacy policy](https://posthog.com/privacy) for the provider's
processing and [data controls](https://posthog.com/docs/privacy/data-storage).

Apple may process App Store or TestFlight diagnostics and feedback according to
your Apple settings and the applicable Apple terms. Information you voluntarily
send through TestFlight or support may be made available to the app operator.

## Calls, speech, and copied information

Choosing Call passes the selected number to the native telephone interface. You
must confirm in the system interface before a call is placed. Apple and your
telephone provider handle any completed call.

Phrase playback uses the device's speech synthesis and available system voices.
The app does not record your microphone. Copy actions place the selected text,
address, coordinates, or number on the system clipboard. Information you paste
or share elsewhere is then handled by the recipient app or service.

## Support and retention

If you contact us, we receive the contact information and message or attachments
you choose to provide. We use those details to respond and investigate the
reported issue. Avoid sending exact location, sensitive information, or private
phone numbers in screenshots unless necessary for your request.

We retain support messages and attachments for as long as needed to respond to your request and follow up on the reported issue. You can request deletion by email. We delete correspondence when it is no longer needed, unless retention is required for legal obligations or resolving a dispute. Gmail and Apple may retain their own service records under their policies.
Contact **[vge2606@gmail.com](mailto:vge2606@gmail.com)** to request access, correction, or deletion
of information you have provided to the operator, subject to applicable law and
any relevant service limitations. If you post feedback in a public forum,
others may see it; use the private contact for personal matters.

## Your choices

- Decline location or change permission in iOS Settings.
- Select a country manually and browse bundled or saved reference data offline.
- Choose whether to request a reference-data download using Pull latest.
- Choose whether to open maps, official websites, a telephone prompt, or copy text.
- Choose what to include in support or TestFlight feedback.

The app is a general travel reference, not a service specifically designed for
children. Its App Store age rating is determined separately through Apple's
content questionnaire. This policy makes no “all ages” or “no data transmitted”
claim.

## Changes and contact

We will update this page when the app's privacy practices change. Questions about
this policy can be sent to **[vge2606@gmail.com](mailto:vge2606@gmail.com)** for
**Vincent Ge**. Support page: **[JourneyMate support](https://gewenyu99.github.io/journeymate-support/support.html)**.
