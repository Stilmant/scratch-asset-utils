### Instructions for Using the Asset Processing Tool

This tool supports one-click import of assets such as backgrounds, costumes, sounds, and sprites. It automatically generates thumbnails and updates the index.

#### Environment Requirements

-   **Runtime Environment**: Python 3.x
-   **Dependencies**: Pillow, shutil, pysocks

#### How to Use

1.  By default, the tool uses the built-in asset library. Alternatively, configure the relevant path parameters.
2.  Execute the script using:

    ```bash
    python scratch2-asset-process.py
    ```

3.  Drag files into the window to add assets automatically. The asset name defaults to the file name.\
    Dragging a folder will automatically process all files within it.

#### Asset Format Requirements

-   **Background Assets**:\
    JPG format, recommended size 480x320
-   **Costume Assets**:\
    PNG or SVG format
-   **Sound Assets**:\
    WAV format
-   **Sprite Assets**:\
    SPRITE2 format

* * * * *

### Instructions for Using the Official Asset Library Crawler

This tool is used to crawl the asset libraries from the official Scratch 2 and Scratch 3 CDNs.

#### Environment Requirements

-   **Runtime Environment**: Python 3.x
-   **Dependencies**: requests

#### How to Use

-   **To Crawl Scratch 2 Asset Library**:\
    Simply execute:

    ```bash
    python scratch2-asset-crawl.py
    ```

-   **To Crawl Scratch 3 Asset Library**:\
    Due to slow download speeds from international resources, the crawler uses a SOCKS proxy. Replace the proxy configuration with your own.\
    Place the latest index file into the `scratch3/json_index` folder and run:

    ```bash 
    python scratch3-asset-crawl.py
    ```

-   **Upload to Cloud Storage**:\
    Using Qiniu Cloud's QSunSync client as an example:

    -   Configure the Access Key (AK) and Secret Key (SK).
    -   Select the `scratch3` folder.
    -   Choose the target storage space.
    -   Click "Start Sync" to begin the upload.
