<template>
    <div class="max-w-7xl mx-auto justify-between text-center items-center py-12">
        <PageHeader title="heyo" class="font-bold text-6xl text-gray-700 py-3" />

        <!-- Description -->
        <p class="text-lg text-black mb-8">
            Fun fact: If you send me your favorite .gif and/or favorite emoji, I'm 15x more likely to respond. 
            
        </p>

        <!-- Contact Form -->
        <form class="bg-green-800/60 shadow-lg rounded-lg p-6 space-y-6">
            <!-- Name Field -->
            <div>
                <label for="name" class="block text-2xl font-medium text-white">name</label>
                <input
                    type="text"
                    id="name"
                    name="name"
                    class="mt-5 block w-full border-gray-800 rounded-md shadow-md focus:ring-green-900/80 focus:border-green-900/80 py-4"
                    placeholder="   your nickname"
                />
            </div>

            <!-- Email Field -->
            <div>
                <label for="email" class="block text-2xl font-medium text-white">email</label>
                <input
                    type="email"
                    id="email"
                    name="email"
                    class="mt-5 block w-full border-gray-300 rounded-md shadow-md focus:ring-green-900/80 focus:border-green-900/80 py-4"
                    placeholder="   your early-2000s-form-of-communication address"
                />
            </div>

            <!-- Message Field -->
            <div>
                <label for="message" class="block text-2xl font-medium text-white">message</label>
                <textarea
                    id="message"
                    name="message"
                    rows="4"
                    class="mt-5 block w-full border-gray-300 rounded-md shadow-md focus:ring-green-900/80 focus:border-green-900/80 py-4"
                    placeholder="   your words and emoticons"
                ></textarea>
            </div>

            <!-- Submit Button -->
            <div>
                <button
                    type="submit"
                    class="w-full bg-green-900/80 hover:bg-gray-800 text-white font-bold py-2 px-4 rounded"
                    href="mailto:loopgallery.mp4@gmail.com"
                >
                    say heyo back
                </button>
            </div>
        </form>
        <!-- Social Media Links -->
        <div class="mt-12 flex justify-center space-x-6">
            <!-- Instagram -->
            <a href="https://www.instagram.com/kendall.gray" target="my instagram" class="hover:opacity-60">
                <img src="https://www.iconpacks.net/icons/2/free-instagram-logo-icon-3497-thumb.png" alt="Instagram" class="h-10 w-10" />
            </a>

             <!-- Email -->
             <a href="mailto:loopgallery.mp4@gmail.com" class="text-lg text-gray-700 hover:text-gray-900 flex-wrap-reverse">
                loopgallery.mp4@gmail.com
            </a>

        </div>
    </div>
</template>