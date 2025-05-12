<template>
    <div class="max-w-=7xl mx-auto justify-between text-center items-center py-12 p-3">
        <!-- Using the ProjectsSection component -->
        <LayoutsProjectsSection
            title="stuff I made (:"
            subtitle="A collection of creative projects I've worked on over the years"
            :projects="visibleProjects"
            :showLoadMore="hasMoreProjects"
            loadMoreText="Show More Projects"
            @load-more="loadMoreProjects"
        />
    </div>
</template>

<script setup>
import { ref, computed } from 'vue';


const allProjects = [
    {
        image: "/overthinkybookclip.gif",
        title: "the overthinky book",
        description: "When I was sick and homebound for 200+ days, I took my journaling obsession, combined it with one-part therapy tools and two-parts artistic catharsis, and made a book that can be filled out by anyone. A boatload of fun to existential questions; by the end of it, you'll know more about yourself. I'll bet you two orders of french fries.",
        link: "https://a.co/d/hQ1oZOt",
        target: "Overthinky Journal Prompt Book",

    },
    {
        image: "/docuclip.gif",
        title: "the documentary",
        description: "In 2020, I decided to write, record, mix and master my first album 80-90% solo. By the time it was completed, I had documented the entire experience, including what I learned. In case you're curious, it was awesome.",
        link: "https://www.youtube.com/watch?v=7Mrbd14T5Tg",
        target: "It's the Documentary",

    },
    {
        image: "/channelclip.gif",
        title: "the youtube channel",
        description: "I started this channel when I was 12. Now I am a professional video editor with a lot of my dearest and strangest memories saved in .mp4 format. Abracadabra, life is crazy.",
        link: "https://www.youtube.com/watch?v=7Mrbd14T5Tg",
        target: "Documentary Again",
 
    },
    {
        image: "/awfgcoverart.png",
        title: "the album",
        description: "When I was 4, I wished for a guitar and a female guitar teacher. I started writing songs at 5. I've played piano since I was 10. Since then, I'd written (and since unpublished) hundreds of songs, and was never truly connected to them. This, however, I like. I spent 4+ years creating this in the basement bedroom of my parents' house!",
        link: "https://open.spotify.com/album/1SePKD46mKjmAuugWuCXug?si=0iWIyOdySvyKI-m2rjVgQg",
        target: "another word for grateful",

    },
    {
        image: "/foggyavenuesclip.gif",
        title: "the fiction novel",
        description: "During the aforementioned 200-Day-Ailment Chapter, I delved into more creative facilities, where a YA Fiction universe was born with several characters that are much like my closest friends. Main theme: Coming of Age meets self-vs-self meets romance. Subtheme: Parapsychology. Special feature: a cat named Booth.",
        link: "https://a.co/d/73xy1e9",
        target: "I wrote a YA fiction novel",

    },
    {
        image: "/muralclip.gif",
        title: "1 of 3 sharpie murals",
        description: "When I was 18, in my childhood bedroom, I vandalized my own walls with permanent marker. From ceiling to floor, I think I captured the essense of my day-to-day thoughts. (My apologies to the future homeowners, but also- you're welcome.)",
        link: "https://youtu.be/gli7wnFO82U?si=GqzbOXLEYxaEPPKS",
        target: "don't trust me with markers",

    }
];

// Initially show only 3 projects
const displayCount = ref(6);

// Computed property for visible projects
const visibleProjects = computed(() => {
    return allProjects.slice(0, displayCount.value);
});

// Computed property to check if there are more projects to load
const hasMoreProjects = computed(() => {
    return visibleProjects.value.length < allProjects.length;
});

// Function to load more projects
const loadMoreProjects = () => {
    displayCount.value += 3;
};
</script>