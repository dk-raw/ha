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
