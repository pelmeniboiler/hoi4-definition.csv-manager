# HOI4 Province Editor

A simple browser-based tool for editing Hearts of Iron IV `definition.csv` files. This editor allows you to easily load, modify, and add new provinces, automatically generating unique RGB colors essential for mapping in `provinces.bmp`.

## Features

* **Load Existing `definition.csv`**: Drag and drop your `definition.csv` file to load existing province data.
* **Interactive Table Editing**: View and edit province data (ID, RGB color, Type, Coastal, Terrain, Continent) in an intuitive spreadsheet-like interface powered by Handsontable.
* **Add New Provinces**:
    * Specify the quantity of new provinces to add.
    * Set default characteristics for these new provinces:
        * Type (land, sea, lake)
        * Coastal status (true, false)
        * Terrain (forest, hills, mountain, plains, etc.)
        * Continent ID
    * New provinces are automatically assigned the next available IDs.
* **Unique Color Generation**: Automatically generates new, unused RGB color combinations for each new province added. This helps prevent color conflicts when editing your `provinces.bmp` map file.
* **Color Swatch & HEX Copy**: Displays a visual color swatch for each province and its corresponding HEX code. Click the swatch to instantly copy the HEX code to your clipboard, ready to be used in your image editor for `provinces.bmp`.
* **Export to CSV**: Export your changes back into a `definition.csv` file format, ready to be used in your HOI4 mod.

## How to Use

1.  [Go to my website](https://pelmeniboiler.github.io/definitionviewer.html) or download the html file and run it.
2.  **Load Data**:
    * Drag your existing `definition.csv` file onto the "Drag your `definition.csv` file here" zone.
    * The province data will be loaded into the editable table.
3.  **Add New Provinces (Optional)**:
    * In the "Control Panel" section:
        * Select the desired 'Type', Coastal status, and Terrain from the dropdown menus.
        * Enter Continent ID.
        * Specify how many New Provinces you want to add.
    * Click the "Add Provinces" button. New rows will appear at the bottom of the table with generated IDs, unique colors, and your chosen default values.
4.  **Edit Data**:
    * Click on any cell in the table to edit its value.
    * You can change RGB values, type, coastal status, terrain, and continent ID for any province.
    * **Note**: If manually changing RGB values, ensure they remain unique and correspond correctly to your `provinces.bmp`.
5.  **Copy Colors**:
    * The 'Swatch' column shows a preview of the province color and its HEX code (e.g., `#FF0000`).
    * Click on any color swatch to copy its HEX code to your clipboard. This is useful for finding and painting the correct color in your `provinces.bmp` file using an image editor (like GIMP or Photoshop).
6.  **Export Data**:
    * Once you are satisfied with your changes, click the "Export CSV" button.
    * A new `definition.csv` file will be downloaded to your computer.

## Important Notes

* **Backup Your Files**: Always back up your original `definition.csv` and `provinces.bmp` files before making significant modifications.
* **Color Uniqueness**: The tool ensures unique colors for *newly generated* provinces. If you manually edit RGB values, it's your responsibility to ensure they don't clash with existing ones or vanilla colors you might not have in your current CSV.
* **Local Processing**: All processing is done client-side in your browser. No data is uploaded to any server.

## Technical Details

* Uses [PapaParse](https://www.papaparse.com/) for CSV parsing and unparsing.
* Uses [Handsontable](https://handsontable.com/) for the interactive grid/table display.

---

This tool is intended to streamline the often tedious process of managing province definitions and color assignments for HOI4 map modding.
