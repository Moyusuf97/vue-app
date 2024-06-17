<template>
  <div>
    <Notification
      v-if="notifications.notificationMessage.showNotifications"
      :message="notifications.notificationMessage"
    />
    <NavbarVue
      :products="desktopMenu.products"
      :articles="desktopMenu.article"
      :category="desktopMenu.category"
      :help="desktopMenu.helpLink"
      :login="desktopMenu.loginLink"
    />

    <!-- <TeaserImage
      v-for="image in desktopMenu.teaserImages.first"
      :key="image.Heading"
      :image="image"
    />
    <TeaserImage
      v-for="image in desktopMenu.teaserImages.second"
      :key="image.Heading"
      :image="image"
    /> -->

    <div class="bg-[url('./heroimg.png')] bg-cover py-40">
      <div class="max-w-6xl mx-auto px-6">
        <div class="max-w-2xl">
          <h1
            class="font-semibold sm:leading-snug text-white text-4xl md:text-5xl"
          >
            Spärra körkort eller annan ID-handling till UC
          </h1>
          <p class="text-white text-xl pt-4 font-medium">
            Minska risken för bedrägerier med tjänsten Förlustanmälan, och anmäl
            ditt borttappade körkort eller ID-kort!
          </p>
        </div>
      </div>
    </div>
    <div class="bg-white">
      <div
        class="max-w-7xl flex md:flex-row items-center justify-center md:items-start md:justify-start px-6 md:px-28 md:px-6 flex-col mx-auto gap-8 py-28"
      >
        <div class="text-[#555555] lg:w-[1800px] text-[17px]">
          <h1 class="text-2xl font-semibold">Hur funkar Förlustanmälan?</h1>
          <p class="pt-2">
            Om du förlorat ditt ID-kort, körkort eller pass bör du anmäla det
            direkt till oss på UC. Då minskar risken för dig att bli utsatt för
            bedrägerier.
          </p>
          <p class="py-5">
            Alla som är folkbokförda i Sverige, och är över 16 år, kan
            förlustanmäla borttappad eller stulen ID-handling till oss på UC.
            Det gör du genom att ringa vår automatiska telefontjänst, dygnet
            runt,
            <span class="font-semibold">0900-101 20 30.</span>
            Samtalet kostar 95 kr. Tjänsten fungerar inte med kontantkort.
          </p>
          <p class="">
            Beställer du
            <a href="#" class="underline text-[#0384B6]"> UC ID-Skydd </a>
            så bjuder vi dig på Förlustanmälningsavgiften (95 kr) - för att
            beställa, ring UC Kundservice på telefon: 0771-20 22 77.
          </p>
          <div class="pt-6">
            <h1 class="text-lg font-semibold">
              Förlustanmälan - en enkel åtgärd som ger bra skydd.
            </h1>
            <ul class="list-disc py-6 px-6">
              <li>
                Du ringer till UC automatiska telefontjänst och anmäler
                borttappad eller stulen ID-handling. Dygnet runt. Samtalet
                kostar 95 kr, vilket dras på din telefonräkning.
              </li>
              <li>
                Vi lägger in en notering om förlorad ID-handling i din
                kreditupplysning.
              </li>
              <li>
                När ett företag tar en kreditupplysning från UC på dig ser de
                att du förlorat din ID-handling. På så sätt kan företaget
                upptäcka om personen som använder din ID-handling försöker
                missbruka den.
              </li>
              <li>
                Du själv kan dock legitimera dig med annan eller ny
                legitimation.
              </li>
              <li>
                Vår notering om förlorad ID-handling ligger kvar i två år.
              </li>
              <li>
                Du kan närsomhelst återkalla uppgifterna om du tex själv hittar
                din ID-handling. Vill du häva din spärr använder du den blankett
                du fick skickad till dig när spärren aktiverades.
              </li>
              <li>
                Pass och andra ID-handlingar bör även förlustanmälas hos Polisen
                för att det ska spärras som resehandling.
              </li>
            </ul>
            <p class="pt-2">
              När vi registrerat förlustanmälan i din kreditupplysning gör
              kreditgivare en extra kontroll. Då kan de vara säkra på att det är
              du, och ingen annan, som ansöker om en kredit. Och du kan vara
              säker på att ingen okänd kan använda din ID-handling utan risk att
              kontrolleras.
            </p>
          </div>
        </div>
        <div class="flex flex-col gap-6">
          <div class="bg-[#F5EBE6] pt-8 pb-10 md:pb-20 rounded-md px-6">
            <h1 class="text-xl font-semibold">Anmäl förlust</h1>
            <p class="py-2">
              Ring vår automatiska telefontjänst, dygnet runt. Samtalet kostar
              95 kr. Tjänsten fungerar inte med kontantkort.
            </p>
            <h1 class="text-lg font-semibold">0900-101 20 30</h1>
            <p class="py-2">
              Om du befinner dig utomlands når du förlustanmälan på nedanstående
              nummer.
            </p>
            <h1 class="font-semibold">+46 900-101 20 30</h1>
          </div>
          <div class="bg-[#F5EBE6] pt-8 md:pb-20 pb-10 rounded-md px-6">
            <div class="flex gap-2 text-2xl font-semibold">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="30"
                height="30"
                viewBox="0 0 16 16"
              >
                <path
                  fill="currentColor"
                  d="M6.457 1.047c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0 1 14.082 15H1.918a1.75 1.75 0 0 1-1.543-2.575Zm1.763.707a.25.25 0 0 0-.44 0L1.698 13.132a.25.25 0 0 0 .22.368h12.164a.25.25 0 0 0 .22-.368Zm.53 3.996v2.5a.75.75 0 0 1-1.5 0v-2.5a.75.75 0 0 1 1.5 0M9 11a1 1 0 1 1-2 0a1 1 0 0 1 2 0"
                />
              </svg>
              Redan utsatt för <span class="flex md:hidden">bedrägeri</span>
            </div>
            <p class="font-semibold text-2xl md:flex hidden pt-[2px]">
              bedrägeri?
            </p>
            <p class="md:py-2 py-4">
              Är du redan utsatt för ett bedrägeri kan det vara en god idé att
              helt spärra din kreditupplysning hos UC. Då minskar du risken för
              fortsatta bedrägerier.
            </p>
            <button
              class="bg-[#F29008] text-white w-full md:w-auto py-1.5 font-medium px-7 rounded-md transition-all hover:bg-[#EF7E00] duration-500"
            >
              Beställ här!
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import DropdownMenu from "../components/DropdownMenu.vue";
import TeaserImage from "../components/TeaserImage.vue";
import Notification from "../components/Notification.vue";
import NavbarVue from "../components/Navbar.vue";
import axios from "axios";

const initialMenuData = {
  mobileMenu: [],
  desktopMenu: {
    products: {
      first: {
        title: "Din information ",
        menuItems: [
          {
            url: "/kreditkollen",
            title: "Kreditkollen",
            name: "Kreditkollen",
            fontAwesomeClass: "far fa-analytics",
            teaserText: "Obegränsad tillgång till din kreditinformation",
          },
          {
            url: "/min-upplysning",
            title: "Min Upplysning",
            name: "Min upplysning",
            fontAwesomeClass: "far fa-lightbulb",
            teaserText: "Komplett nulägesrapport om din kreditinformation",
          },
          {
            url: "/mitt-kreditbetyg",
            title: "Mitt Kreditbetyg",
            name: "Mitt Kreditbetyg",
            fontAwesomeClass: "far fa-tachometer",
            teaserText: "Tillgång till ditt kreditbetyg i en vecka",
          },
          {
            url: "/digital-brevlada",
            title: "Digital Brevlåda",
            name: "Digital brevlåda",
            fontAwesomeClass: "fas fa-envelope",
            teaserText: "Gratis",
          },
        ],
      },
      second: {
        title: "Känn dig trygg",
        menuItems: [
          {
            url: "/id-skydd",
            title: "ID-Skydd",
            name: "ID-Skydd",
            fontAwesomeClass: "far fa-user-shield",
            teaserText: "Löpande bevakning av dina personliga uppgifter",
          },
          {
            url: "/forlustanmalan",
            title: "Förlustanmälan",
            name: "Förlustanmälan",
            fontAwesomeClass: "far fa-phone",
            teaserText: "Anmäl borttappade ID-handlingar",
          },
          {
            url: "/bedragerisparr",
            title: "Bedrägerispärr",
            name: "Bedrägerispärr",
            fontAwesomeClass: "far fa-shield",
            teaserText: "Spärra din kreditupplysning",
          },
        ],
      },
    },
    article: {
      title: "Särskilt utvalda artiklar",
      menuItems: [
        {
          url: "/riskprognos",
          title: "UC Riskprognos",
          name: "UC Riskprognos",
          fontAwesomeClass: null,
          teaserText: null,
        },
        {
          url: "/hur-jobbar-en-id-kapare",
          title: "Vad är identitetsstöld?",
          name: "Vad är identitetsstöld?",
          fontAwesomeClass: null,
          teaserText: null,
        },
        {
          url: "/kreditupplysning-privatperson",
          title: "Om kreditupplysning privatperson",
          name: "Om kreditupplysning privatperson",
          fontAwesomeClass: null,
          teaserText: null,
        },
        {
          url: "/kreditvardighet",
          title: "Om kreditvärdighet",
          name: "Om kreditvärdighet",
          fontAwesomeClass: null,
          teaserText: null,
        },
        {
          url: "/betalningsanmarkning",
          title: "Om betalningsanmärkning",
          name: "Om betalningsanmärkning",
          fontAwesomeClass: null,
          teaserText: null,
        },
      ],
    },
    category: {
      title: "Kategorier",
      menuItems: [
        {
          url: "/privatekonomi",
          title: "Alla artiklar",
          name: "Alla artiklar kring privatekonomi",
          fontAwesomeClass: "far fa-book",
          teaserText: null,
        },
        {
          url: "/privatekonomi",
          title: "Privatekonomi",
          name: "Privatekonomi",
          fontAwesomeClass: "far fa-user-graduate",
          teaserText: null,
        },
        {
          url: "/id-stold",
          title: "ID-Stöld",
          name: "ID-Stöld",
          fontAwesomeClass: "far fa-user-shield",
          teaserText: null,
        },
      ],
    },
    teaserImages: {
      first: [
        {
          FACode: null,
          Heading: "Vinn ett ID-Skydd",
          BackgroundTheme: "beach",
          TextColorTheme: "white",
          BackgroundImage:
            "/contentassets/781cd9372c194a7fb176d81d70317a28/vinn-ett-id-skydd.png",
          CardSize: "small",
          VerticalAlign: "top",
          SectionTextAlign: "left",
          SectionText:
            "\u003Cp\u003EUndvik ID-kaparen och samla po&auml;ng genom att f&aring;nga ID-skyddet.\u003C/p\u003E",
          ButtonBlocks: [
            {
              NDSButtonSize: "default",
              NDSButtonVariant: "primary",
              NDSOnBg: "light",
              Heading: "Till spelet",
              IsSubHeading: false,
              SubHeading: null,
              CtaUrl: "https://www1.minuc.se/id-skydd/vinn-id-skydd",
              ButtonSize: "default",
              ColourTheme: "sectiongray",
              IsBadge: false,
              BadgeColour: "blue",
              BadgeTopText: null,
              BadgeMidText: null,
              BadgeBottomText: null,
              ButtonText: "Till spelet",
            },
          ],
        },
      ],
      second: [
        {
          FACode: null,
          Heading: "Hur tryggt är ditt personnummer?",
          BackgroundTheme: "beach",
          TextColorTheme: "white",
          BackgroundImage: "/globalassets/idsmart-popup.png",
          CardSize: "small",
          VerticalAlign: "top",
          SectionTextAlign: "left",
          SectionText:
            '\u003Cp\u003EG&ouml;r v&aring;rt test p&aring; \u003Ca href="http://idsmart.se" target="_blank" rel="noopener"\u003E\u003Cstrong class="ContentLuminous"\u003Eidsmart.se\u003C/strong\u003E\u003C/a\u003E och se sj&auml;lv.\u003C/p\u003E',
          ButtonBlocks: [
            {
              NDSButtonSize: "default",
              NDSButtonVariant: "primary",
              NDSOnBg: "light",
              Heading: "Gå till testet!",
              IsSubHeading: false,
              SubHeading: null,
              CtaUrl: "http://www.idsmart.se/",
              ButtonSize: "default",
              ColourTheme: "sectiongray",
              IsBadge: false,
              BadgeColour: "blue",
              BadgeTopText: null,
              BadgeMidText: null,
              BadgeBottomText: null,
              ButtonText: "Gå till testet!",
            },
          ],
        },
      ],
    },
    helpLink: "/fragor-svar",
    loginLink: "/logga-in",
  },
  notificationsMessages: {
    loggedInNotificationMessage: {
      title: "OBS! ",
      theme: "Red",
      description:
        '\u003Cp\u003EDetta &auml;r MinUC:s testmilj&ouml;. G&aring; till \u003Ca href="https://minuc.se"\u003Ehttps://www.minuc.se\u003C/a\u003E f&ouml;r att n&aring; den publika webbplatsen.\u003C/p\u003E',
      icon: "fas fa-info",
      showNotifications: true,
    },
    notificationMessage: {
      title: "OBS!",
      theme: "Red",
      description:
        '\u003Cp\u003EDetta &auml;r MinUC:s testmilj&ouml;. G&aring; till \u003Ca href="https://minuc.se"\u003Ehttps://www.minuc.se\u003C/a\u003E f&ouml;r att n&aring; den publika webbplatsen.\u003C/p\u003E',
      icon: "fas fa-info",
      showNotifications: true,
    },
  },
};

const desktopMenu = ref(initialMenuData.desktopMenu);
const notifications = ref(initialMenuData.notificationsMessages);

onMounted(async () => {
  // const response = await fetch("/api/frontendapi/getmenu");
  // const data = await response.json();
  // desktopMenu.value = data.desktopMenu;
  // notifications.value = data.notificationsMessages;

  const getData = async () => {
    try {
      const response = await axios.get(
        "https://www1.minuc.se/frontendapi/getmenu",
        {
          headers: {
            Accept: "application/json",
          },
        }
      );

      desktopMenu.value = response.data.desktopMenu;
      notifications.value = response.data.notificationsMessages;
    } catch (error) {
      console.error("Error fetching menu:", error);
    }
  };

  getData();
});
</script>
