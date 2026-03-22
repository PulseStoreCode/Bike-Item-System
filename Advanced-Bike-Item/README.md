# Bike Item Script – Multi Framework

Deployable bike script compatible with **ESX, QBCore, and Standalone**.

## Features

* ✅ Multi-framework support (ESX, QBCore, Standalone)
* ✅ 7 different bike types
* ✅ Deployment and pickup animations
* ✅ 3D text for pickup interaction
* ✅ Highly detailed configuration
* ✅ Advanced options (locking, invincibility, auto-delete)

---

## Installation

### 1. Framework Configuration

Open `config.lua` and change the line:

```lua
Config.Framework = 'esx'  -- Options: 'esx', 'qbcore', 'standalone'
```

---

### 2. ESX Installation

1. Execute the `items.sql` file in your database
2. Add `ensure bmx_item` to your `server.cfg`
3. Restart the server

---

### 3. QBCore Installation

1. Add the items from `items_qbcore.lua` into `qb-core/shared/items.lua`
2. Add `ensure bmx_item` to your `server.cfg`
3. Restart the server

---

### 4. Standalone Installation

1. Add `ensure bmx_item` to your `server.cfg`
2. Use the command `/givebike [type]` to receive a bike

   * Example: `/givebike bmx`
3. Restart the server

---

## 🚲 Available Bike Types

* `bmx` – BMX
* `cruiser` – Cruiser (beach bike)
* `fixter` – Fixter (fixie bike)
* `scorcher` – Scorcher MTB
* `tribike` – TriBike Race
* `tribike2` – TriBike Sport
* `tribike3` – TriBike Pro

---

## ⚙️ Configuration

All options are located in `config.lua`:

* Display and pickup distances
* Pickup key
* 3D text style
* Customizable animations
* Per-bike options (spawn distance, weight, enabled state)
* Advanced options (auto-delete, locking, invincibility)

---

## Usage

1. Use the bike item from your inventory
2. The bike will deploy in front of you with an animation
3. Use the bike normally
4. Get off and press `E` to pick it up
5. The bike returns to your inventory

---

## Support

To add a new bike, add it in `config.lua`:

```lua
['bike_name'] = {
    label = 'Bike Name',
    model = 'gta_model',
    spawnDistance = 2.0,
    weight = 5,
    enabled = true
}
```

Don't forget to add the item to your **database or items file**!

