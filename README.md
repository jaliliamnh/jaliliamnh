







- 
-  
-









#---------------------------
I
# -------------------------
"          ."
O"           e.g.inu
branch = "main"          #r the default branch you need
# If the repo is private, set a oken here:
# token = "ghp_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
# headers = {"Authorization": fken {token}"}
ers = {}  lic repoeds no auh

# ----------------------------
# 2️⃣ ETCH P ARCHIVE (quickest way to get the whole repo)
# ----------------------------
ip_url = f"https://api.github.com/repos/{owner}/{repo}/zipball/{branch}"
resp = requests.get(zip_url, headers=headers)
ise_for_status()

# Unpack the zip into a local folder
zip_bytes = io.BytesIO(resp.content)
with zipfile.ZipFile(zip_bytes) as z:
    # The zip contains a top‑level folder like "owner-repo-<hash>"
    # Extract everything into a folder named after the repo
    extract_path = f"./{repo}"
    os.makedirs(extract_path, exist_ok=True)
    z.extractall(path=extract_path)

rint(f"✅  Repository '{owner}/{repo}' extracted to ./{repo}")



