# YachtFinder

Research yachts the way a professional does, inside your assistant. This plugin pairs YachtFinder's connector with three skills that teach the assistant how a broker, a buyer's agent or an analyst works with YachtFinder's records of yachts for sale, for charter and reported sold.

## What it adds

- **The YachtFinder connector** (`https://mcp.yachtfinder.co/mcp`, the same server as the YachtFinder connector in the directory): three read-only tools that find yachts by builder, length, asking price, build year, status and place; list the yachts whose latest published AIS position is near a harbour, an anchorage or a coordinate; and give one yacht's facts with the source and date of each. A fourth tool, `prepare_inquiry`, prepares a request about one yacht for you to send: it saves a draft and gives you one link to it on yachtfinder.co. It never sends anything: you read and edit the draft there, sign in, and only your tap on Send sends it.
- **Check a yacht before an offer** (`check-a-yacht`): her record, how her asking price sits against YachtFinder's estimate and against similar yachts for sale and reported sold, conflicts between where her listing says she is and where AIS last placed her, and the questions to put to her broker.
- **Build a charter shortlist** (`charter-shortlist`): yachts for charter by size, guests, budget and place, with each published weekly rate and its season, and where each was last seen.
- **Write a market brief** (`market-brief`): for a builder, a length or price band, or a place, how many yachts are for sale, the asking-price range and median, how many are price on application, how many are reported sold, and the notable yachts.

## Use it

Ask in your own words, for example:

- "I'm thinking of making an offer on Lady Lara. What should I check first?"
- "Shortlist yachts I could charter in Greece next summer for 10 guests, 40 to 50 metres."
- "Give me a market brief on Benetti yachts between 40 and 50 metres for sale."
- "Prepare a request to Lady Lara's broker asking about her last survey." (You get a link to the draft; nothing is sent until you sign in on yachtfinder.co and tap Send.)

Every figure in an answer comes from YachtFinder's records, with the date the catalogue was built and a link to each yacht's page on yachtfinder.co. An asking price is always the broker's asking price, never a sale price; the plugin's tools return no sale prices. YachtFinder's estimate is a model, not an appraisal. A position is an AIS fix with its time. When a fact is not in the record, the answer says so instead of guessing.

## Data

The skills are written instructions only; the plugin runs no code and stores nothing. When a skill looks something up, the assistant sends the search terms (a yacht's name, a builder, lengths, prices, a harbour) to `https://mcp.yachtfinder.co/mcp`. The connector needs no account. For a lookup it returns yacht records only and does not record your question or your network address; its own logs hold which tool ran, how many yachts matched, how long it took, and errors. One tool is different: when you ask the assistant to prepare a request to a yacht's broker, the connector keeps that draft (the yacht, your dates and up to five questions the assistant wrote) for 24 hours, so the link can open it on yachtfinder.co. It is deleted when you send the request, and in any case after 24 hours. Cloudflare, which hosts it, keeps standard request logs, as the privacy policy describes. In Claude Code the request comes from your computer; in claude.ai, Cowork and the apps it comes from the assistant's servers. Details: [the connector's page](https://mcp.yachtfinder.co/) and the [YachtFinder privacy policy](https://yachtfinder.co/privacy). Answers are provided under the [YachtFinder terms](https://yachtfinder.co/terms).

The assistant never contacts a broker, books, pays or sends anything on your behalf. It looks things up and drafts. A prepared request goes to a broker only when you sign in on yachtfinder.co and press Send.

## Support

Email info@yachtfinder.co, or see [yachtfinder.co/support](https://yachtfinder.co/support).

## License

The files in this plugin are under the MIT License (see `LICENSE`). YachtFinder's data, reached through the connector, is provided under the [YachtFinder terms](https://yachtfinder.co/terms).
