## Project Highlights

- **Go + Kubernetes Personal Data Server (PDS)**  
  Implements a simplified Personal Data Server inspired by the AT Protocol: per‑user repositories, signed records, and revision tracking exposed via XRPC-style HTTP endpoints.  
  - AT Protocol overview: https://atproto.com/guides/overview  
  - PDS / repository concepts: https://atproto.com/specs/repository

- **MariaDB‑backed, multi‑tenant data model**  
  Stores accounts, repositories, records, and commits in a shared MariaDB instance, with clear boundaries between users and deterministic hashing of record contents for integrity checks.

- **React + TypeScript web client**  
  Single‑page application for signing in, composing posts, viewing feeds, and managing integrations, talking exclusively to the Go PDS API over HTTPS.

- **Bluesky / AT Protocol comment integration (aspirational)**  
  Treats each post as an AT Protocol record so that external Bluesky clients can reply, with plans to surface those replies in the UI by querying Bluesky’s AppView thread APIs.  
  - Bluesky / AT Protocol docs: https://docs.bsky.app/docs/advanced-guides/atproto

- **ActivityPub comments via Pinka (aspirational)**  
  Uses Pinka as an ActivityPub‑powered commenting layer, enabling users on Mastodon and other Fediverse platforms to reply to posts and have their comments appear alongside local discussion.  
  - Pinka: https://pinka.dev/  

- **Cross‑posting to photo platforms (aspirational)**  
  Background worker service designed to cross‑post selected posts (image + metadata) to external photo‑sharing platforms such as Flickr and Pixelfed using their public APIs.  
  - Flickr API: https://www.flickr.com/services/api/  
  - Pixelfed: https://github.com/pixelfed/pixelfed  

- **AI‑assisted development workflow**  
  Intentionally developed with AI coding assistants to accelerate boilerplate, tests, and infrastructure configuration, while keeping protocol logic, cryptography, and architecture decisions under careful human review.