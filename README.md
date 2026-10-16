# ITS EDITOR NITIN — portfolio site

This is a dependency-free static portfolio. Open `index.html` in a browser. The hero scrubs the supplied 302-frame, 30 fps sequence in `frames-30fps/` as the page scrolls.

## Add project videos

Copy each video into `assets/projects/` beside `index.html`, then edit the matching entry in `project-data.js`. The data file has four categories and five project entries in each. Update only the fields you need:

- `title`: optional title shown on a card with a video and in its hover panel
- `video`: relative local file path for a video you have copied into `assets/projects/`
- `poster`: optional relative poster image path
- `link`: optional project URL shown in the hover panel

Leave `video` empty until the file exists. Empty slots render as clean dark cards without text or badges. Video previews autoplay muted while visible and loop with `object-fit: cover`. Click a video or its sound icon to toggle audio; turning on one preview mutes the others. The gallery keeps four independent infinite rows moving right, left, right, left. Loop copies do not add project slots.

## Update portfolio details

Edit visible text in `index.html` for the about copy, services, testimonials, and contact details. The inquiry form prepares an email to `itseditornitin@gmail.com`; it does not send or store form data on a server.

To replace the animated hero sequence, update `frameCount` and the filename template in the script, and put the numbered WebP frames in the configured folder. The original 192-frame sequence in `frames/` is kept as a backup.

## Deploy on Vercel

The repository root is the static site root. Import this repository in Vercel and deploy with the default static settings; no build command or framework is required. Keep `index.html`, `project-data.js`, `assets/`, `frames/`, and `frames-30fps/` at the repository root so all relative asset URLs resolve. `vercel.json` enables clean URLs and avoids trailing slash variants.
