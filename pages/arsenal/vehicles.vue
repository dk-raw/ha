<template>
  <div class="container">
    <h1>HA Vehicle Arsenal</h1>
    <p class="lead">
      MBTs, APCs, AAVs, ASVs, MLRS, SAMs, UAVs, IFVs, Howitzers, Attack
      Helicopters and other motorized vehicles
    </p>
    <hr />
    <div
      class="row row-cols-1 row-cols-xxl-4 row-cols-xl-3 row-cols-lg-2 row-cols-md-2 row-cols-sm-1 g-4 mb-4"
    >
      <div class="col" v-for="vehicle in vehicles" :key="vehicle.id">
        <Card
          :header="vehicle.header"
          :description="vehicle.description"
          :imageUrl="vehicle.imageUrl"
          :tags="vehicle.tags"
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
      vehicles: [
        {
          header: "Leopard 2A7/2A6 HEL",
          description:
            "21st century Main Battle Tank armed with a Rheinmetall 120mm gun and fitted with enchanced composite armour and a V12 twin-turbo engine outputing 1,103kW with a top spedd of 70km/h.",
          imageUrl: "leopard-2a6.jpg",
          tags: [
            {
              type: "MBT",
            },
          ],
        },
        {
          header: "Leopard 1A4/A5",
          description:
            "Highly modernized and proven Main Battle Tank armed with a 105mm Royal Ordnance L7A3 L/52 rifled gun and fitted with polycarbonate armour. The Leopard has a power-to-weight ratio of 14.5:1 and a top speed of 65km/h.",
          imageUrl: "leopard-1a5.jpg",
          tags: [
            {
              type: "MBT",
            },
          ],
        },
        {
          header: "VBL",
          description:
            "Lightwight, fast and agile armoured vehicle with a top speed of 95km/h. Armed with M2 Browning, M240 machine guns or MILAN II ATGM. Number of the these patrol the Greek-Turkish borders in Evros and were also deployed in Afghanistan.",
          imageUrl: "vbl.jpg",
          tags: [
            {
              type: "ASV",
            },
          ],
        },
        {
          header: "M1114GR/M1119GR HUMVEE",
          description:
            "Multi-purpose vehicle with a top speed of 113km/h. Armed with M2 Browning machine gun, MILAN II or 9K111 ATGM. The HUMVEE is also used to carry the ASRAD HELLAS SHORAD, for transportation or as an ambulance.",
          imageUrl: "humvee.jpg",
          tags: [
            {
              type: "ASV",
            },
          ],
        },
        {
          header: "M113A1/A2",
          description:
            "Fully tracked armored personnel carrier armed with an M2 Browning machine gun carrying 15 troops. It features 28-44mm all-round 5083 alloy armor that protects from small arms fire and a top speed of 68km/h.",
          imageUrl: "m113.jpg",
          tags: [
            {
              type: "APC",
            },
          ],
        },
        {
          header: "M106A1/A2",
          description:
            "Self-propelled mortar carrier armed with a M2 Browning machine gun and a M30 106mm mortar, M29A1 81mm mortar or a E56 120mm mortar. It is based on a M113 APC and can hold 88 mortar rounds with various warheards.",
          imageUrl: "m106.jpg",
          tags: [
            {
              type: "APC",
            },
            {
              type: "Mortar carrier",
            },
          ],
        },
        {
          header: "Lynx KF-41",
          description:
            "Modern and highly advanced infantry fighting vehicle armed with a 35mm autocannon while providing all-round protection from 30mm rounds and ATGMs. It can carry 3+8 soldiers and it's equiped with an electrooptical sensor suite.",
          imageUrl: "lynx.jpg",
          tags: [
            {
              type: "IFV",
            },
          ],
        },
        {
          header: "M1117 Guardian",
          description:
            "Armoured, mine-resistant security vehicle with a top speed of 101km/h. It is equipped with a M2 Browning machine gun, Mk 19 grenade launcher and a MG3 machine gun as a secondary. The Hellenic Army operates 1200 M1117s.",
          imageUrl: "m1117.jpg",
          tags: [
            {
              type: "ASV",
            },
          ],
        },
        {
          header: "Cougar",
          description:
            "Armoured mine-resistant ambush-protected vehicle with a top speed of 105km/h. Will be armed with a M2 Browning or MG3 machine gun and will be used for patrol and armed reconnaissance. The HA will operate 500 Cougars.",
          imageUrl: "cougar.jpg",
          tags: [
            {
              type: "ASV",
            },
          ],
        },
        {
          header: "M270",
          description:
            "US Multiple Launch Rocket System armed with 12 M26 artillery rockets or 2 MGM-140 ATACMS GPS/INS guided rockets with a maximum range of 165km. It can be used to strike enemy vehicles, installations and fortifications.",
          imageUrl: "m270.jpg",
          tags: [
            {
              type: "MLRS",
            },
          ],
        },
        {
          header: "RM70",
          description:
            "Multiple Launch Rocket System armed with 40 artillery rockets with a variety of warheads such as HEAT. It's maximum firing range is 20km. The Hellenic Army operates 111 RM70s that will be upgraded to RM-70 Vampires.",
          imageUrl: "rm70.jpg",
          tags: [
            {
              type: "MLRS",
            },
          ],
        },
        {
          header: "PhZ 2000",
          description:
            "Highly modern and manuverable self-propelled howitzer equiped with a Rheinmetall 155mm cannon. It has a maximum firing range of 60km with the SMArt 155 guided artillery round and can be used with a Sperwer UAV for guidance.",
          imageUrl: "phz-2000.jpg",
          tags: [
            {
              type: "Self-propelled Howitzer",
            },
          ],
        },
        {
          header: "M109A1/A2/A3/A5",
          description:
            "Self-propelled howitzer with a M126 155mm cannon. It has a rate of fire of 1 rpm sustained and a maximum range of 21km. It can also be linked with other M109s or PhZ 2000s for enchanched firepower with coordinated firing.",
          imageUrl: "m109a2.jpg",
          tags: [
            {
              type: "Self-propelled Howitzer",
            },
          ],
        },
        {
          header: "ASRAD HELLAS",
          description:
            "Advanced HUMVEE-mounted short range air defense system with a range of 8km. It fires the STINGER missiles and is equiped with infrared search and track sensors. The Hellenic Army operates 60 ASRAD HELLASs.",
          imageUrl: "asrad.jpg",
          tags: [
            {
              type: "SHORAD",
            },
          ],
        },
        {
          header: "TOR M1",
          description:
            "Advanced HUMVEE-mounted short range air defense system with a range of 8km. It fires the STINGER missiles and is equiped with infrared search and track sensors. The Hellenic Army operates 60 ASRAD HELLASs.",
          imageUrl: "tor.jpg",
          tags: [
            {
              type: "SHORAD",
            },
          ],
        },
        {
          header: "SAGEM Sperwer",
          description:
            "Short range reconnaissance unmaned aerial vehicle capable of delivering real-time thermal and TV images of enemy posotions to it's base while targeting and guiding artillery fire. The Sperwer has a 5 hour endurance.",
          imageUrl: "sperwer.jpg",
          tags: [
            {
              type: "UAV",
            },
            {
              type: "Reconnaissance",
            },
          ],
        },
        {
          header: "AH-64A/D Apache Longbow",
          description:
            "Twin turboshaft attack helicopter featuring target acquisition and designation, a night vision system, infrared countermeasures and a thermographic camera. Armed with AGM-114 or SPIKE NLOS ATGMs and Hydra 70 rockets.",
          imageUrl: "ah64.jpg",
          tags: [
            {
              type: "Attack Helicopter",
            },
          ],
        },
        {
          header: "OH-58 Kiowa Warrior",
          description:
            "Attack helicopter used for armed observation and reconnaissance over the battlefield. It is equiped with AGM-114 ATGMs and Hydra 70 rockets. It also features a thermal imaging and laser range finder/designator system.",
          imageUrl: "oh58.jpg",
          tags: [
            {
              type: "Attack Helicopter",
            },
          ],
        },
        {
          header: "NH-90 TTH",
          description:
            "Multi role tactical military helicopter primarily used for transporting Special Forces Units. It is fitted with an infrared suppression system, wire strike protection system, forward looking infrared and helmet mounted display. The NH90 possesses the lowest radar signature in its class.",
          imageUrl: "nh90.jpg",
          tags: [
            {
              type: "Helicopter",
            },
            {
              type: "Tactical Transport",
            },
          ],
        },
        {
          header: "CH-47DG Chinook",
          description:
            "Twin engine heavy-lift transport helicopter used for transporting heavy payloads and troops in inaccessible areas. It features 2 Lycoming T55-GA-714A turboshaft engines with a combined power output of 7,458 kW. The CH-47 can achieve speeds of up to 170 knots.",
          imageUrl: "ch47.jpg",
          tags: [
            {
              type: "Helicopter",
            },
            {
              type: "Tactical Transport",
            },
          ],
        },
      ],
    };
  },
};
</script>
