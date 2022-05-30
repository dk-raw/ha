<template>
  <div class="container">
    <h1>HA Arms &#38; Weapons Arsenal</h1>
    <p class="lead">
      Rifles, Pistols, Machine Guns, Mortars, Grenade Launchers and ATGMs
    </p>
    <hr />
    <div
      class="row row-cols-1 row-cols-xxl-4 row-cols-xl-3 row-cols-lg-2 row-cols-md-2 row-cols-sm-1 g-4 mb-4"
    >
      <div class="col" v-for="weapon in weapons" :key="weapon.id">
        <Card
          :header="weapon.header"
          :characteristics="weapon.characteristics"
          :description="weapon.description"
          :imageUrl="weapon.imageUrl"
          :tags="weapon.tags"
        />
      </div>
    </div>
    <h4>Other weapons include</h4>
    <ul>
      <li>H&K USP</li>
      <li>Baretta M8</li>
      <li>Colt M1911A1</li>
      <li>Glock 17</li>
      <li>FN FAL</li>
      <li>H&K MP5</li>
      <li>H&K A1</li>
      <li>FN MAG</li>
      <li>Rheinmetall MG3</li>
      <li>M2 Browning</li>
      <li>M60</li>
      <li>Barrett M82A1M</li>
      <li>Barrett M95</li>
      <li>Steyr SSG08</li>
      <li>M6C-210</li>
      <li>M19</li>
      <li>M29</li>
      <li>MO-81-61</li>
      <li>M30</li>
      <li>E44-E1</li>
      <li>E56</li>
      <li>M203/203PI</li>
      <li>H&K GMG</li>
      <li>Mk19 Mod3</li>
      <li>M79 Blooper</li>
      <li>ACL-89 STRIM</li>
      <li>M2 Carl Gustav</li>
      <li>AT4</li>
      <li>M72 LAW</li>
      <li>RPG-18</li>
      <li>M67</li>
      <li>M40A1</li>
      <li>BGM-71 TOW</li>
      <li>MILAN I/II</li>
      <li>9K111 Fagot</li>
      <li>9M133 Kornet E</li>
      <li>Spike NLOS</li>
      <li>FIM-92 Stinger</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Arsenal",
  data() {
    return {
      weapons: [
        {
          header: "H&K G3A3/A4",
          imageUrl: "g3.jpg",
          characteristics: [
            { type: "Cartridge", value: "7.62x51mm NATO" },
            { type: "Rate of fire", value: "600 rounds/min" },
            { type: "Muzzle velocity", value: "800m/s" },
          ],
          description: "Service rifle made under license in Greece",
          tags: [
            {
              type: "Rifle",
            },
          ],
        },
        {
          header: "M16A2/A3/A4",
          imageUrl: "m16.jpg",
          characteristics: [
            { type: "Cartridge", value: "5.56x45 mm NATO" },
            { type: "Rate of fire", value: "700-900 rounds/min" },
            { type: "Muzzle velocity", value: "960m/s" },
          ],
          tags: [
            {
              type: "Rifle",
            },
          ],
        },
        {
          header: "M4A1/A2",
          imageUrl: "m4.jpg",
          characteristics: [
            { type: "Cartridge", value: "5.56x45 mm NATO" },
            { type: "Rate of fire", value: "700-950 rounds/min" },
            { type: "Muzzle velocity", value: "910m/s" },
          ],
          tags: [
            {
              type: "Rifle",
            },
          ],
        },
        {
          header: "Mk 18",
          imageUrl: "mk18.jpg",
          characteristics: [
            { type: "Cartridge", value: "5.56x45 mm NATO" },
            { type: "Rate of fire", value: "700-950 rounds/min" },
            { type: "Muzzle velocity", value: "788m/s" },
          ],
          description: "Used primarily by the Special Forces.",
          tags: [
            {
              type: "Rifle",
            },
          ],
        },
        {
          header: "FN Minimi",
          imageUrl: "minimi.jpg",
          characteristics: [
            { type: "Cartridge", value: "5.56x45 mm NATO" },
            { type: "Rate of fire", value: "700-1,150 rounds/min" },
            { type: "Muzzle velocity", value: "925m/s" },
          ],
          tags: [
            {
              type: "Machine Gun",
            },
          ],
        },
      ],
    };
  },
};
</script>
