# Base directory
base_dir = Path("/mnt/data/InkByDowney")
images_dir = base_dir / "images"

# Create folders
images_dir.mkdir(parents=True, exist_ok=True)

# Copy provided images into the images folder
shutil.copy("/mnt/data/DE6E5AB1-689A-4CCD-96AB-0038E477AADF.jpeg", images_dir / "illustration-1.jpg")
shutil.copy("/mnt/data/24105D07-9163-4FD4-881B-46DF93147B4D.jpeg", images_dir / "illustration-2.jpg")

# Common head section
head_section = """
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <script src="https://cdn.tailwindcss.com"></script>
"""

# index.html
index_html = f"""<!DOCTYPE html>
<html lang="en">
<head>
{head_section}
<title>InkByDowney — Illustrator Portfolio</title>
<meta name="description" content="Cinematic, character-driven illustration for writers and storytellers." />
</head>

<body class="bg-slate-950 text-gray-200 antialiased scroll-smooth">

<header class="fixed w-full bg-slate-950/80 backdrop-blur z-50">
  <nav class="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
    <span class="text-xl font-semibold tracking-wide">InkByDowney</span>
    <div class="space-x-6 text-sm">
      <a href="index.html" class="text-white">Home</a>
      <a href="portfolio.html" class="hover:text-white">Portfolio</a>
      <a href="contact.html" class="hover:text-white">Contact</a>
    </div>
  </nav>
</header>

<main class="pt-28 max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">

<div>
  <h1 class="text-5xl font-bold text-white leading-tight">
    Illustrations That Feel Like Cinema
  </h1>
  <p class="mt-6 text-lg text-gray-400">
    Atmospheric, emotionally-charged artwork designed for writers, novelists, and storytellers who want their worlds visualized with intensity and depth.
  </p>

  <div class="mt-8 flex gap-4">
    <a href="portfolio.html" class="bg-white text-slate-950 px-6 py-3 rounded-md font-medium hover:bg-gray-200 transition">
      View Portfolio
    </a>
    <a href="contact.html" class="border border-gray-500 px-6 py-3 rounded-md hover:border-white transition">
      Commission Work
    </a>
  </div>

  <div class="mt-6 text-sm text-gray-500">
    downeycurtis4@gmail.com
  </div>
</div>

<div>
  <img src="images/illustration-2.jpg" class="rounded-xl shadow-2xl w-full object-cover">
</div>

</main>

<footer class="py-10 text-center text-sm text-gray-600 mt-24">
© 2026 InkByDowney. All rights reserved.
</footer>

</body>
</html>
"""

# portfolio.html
portfolio_html = f"""<!DOCTYPE html>
<html lang="en">
<head>
{head_section}
<title>Portfolio — InkByDowney</title>
</head>

<body class="bg-slate-950 text-gray-200">

<header class="fixed w-full bg-slate-950/80 backdrop-blur z-50">
  <nav class="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
    <span class="text-xl font-semibold">InkByDowney</span>
    <div class="space-x-6 text-sm">
      <a href="index.html" class="hover:text-white">Home</a>
      <a href="portfolio.html" class="text-white">Portfolio</a>
      <a href="contact.html" class="hover:text-white">Contact</a>
    </div>
  </nav>
</header>

<main class="pt-28 max-w-7xl mx-auto px-6">
<h1 class="text-4xl font-bold text-white mb-12">Selected Works</h1>

<div class="grid sm:grid-cols-2 gap-10">
  <img src="images/illustration-1.jpg" class="rounded-xl shadow-xl hover:scale-[1.02] transition duration-300">
  <img src="images/illustration-2.jpg" class="rounded-xl shadow-xl hover:scale-[1.02] transition duration-300">
</div>

</main>

<footer class="py-10 text-center text-sm text-gray-600 mt-24">
© 2026 InkByDowney
</footer>

</body>
</html>
"""

# contact.html
contact_html = f"""<!DOCTYPE html>
<html lang="en">
<head>
{head_section}
<title>Contact — InkByDowney</title>
</head>

<body class="bg-slate-950 text-gray-200">

<header class="fixed w-full bg-slate-950/80 backdrop-blur z-50">
  <nav class="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
    <span class="text-xl font-semibold">InkByDowney</span>
    <div class="space-x-6 text-sm">
      <a href="index.html" class="hover:text-white">Home</a>
      <a href="portfolio.html" class="hover:text-white">Portfolio</a>
      <a href="contact.html" class="text-white">Contact</a>
    </div>
  </nav>
</header>

<main class="pt-28 max-w-3xl mx-auto px-6 text-center">
<h1 class="text-4xl font-bold text-white mb-6">Let’s Collaborate</h1>

<p class="text-gray-400 mb-10">
For commissions, cover art, or collaborations, email me directly.
</p>

<a href="mailto:downeycurtis4@gmail.com"
class="inline-block bg-white text-slate-950 px-8 py-4 rounded-lg font-semibold hover:bg-gray-200 transition">
downeycurtis4@gmail.com
</a>

</main>

<footer class="py-10 text-center text-sm text-gray-600 mt-24">
© 2026 InkByDowney
</footer>

</body>
</html>
