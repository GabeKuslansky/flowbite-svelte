---
layout: doc
---

<script>
  import { SmallModal, ModalButton, modalIdStore }from '$lib/index';
  import { goto } from "$app/navigation";

  const closeModal = () => {
    modalIdStore.update((value) => {
      value = null;
    });
  };

  // for basic
  const idBasic = "basic-modal";
  const btnBasicName = "Basic Modal";

  // for small modal 1
  const btnName1 = "Small Modal";
  const id1 = "small-modal";
  const btnColor1 = "purple";

  const handlebtnS1 = () => {
    closeModal()
    goto("/about");
  };

  const handlebtnS2 = () => {
    closeModal()
  };

  // for small modal 2
  const btnName2 = "Small Modal 2";
  const id2 = "small-modal-2";
  const btnColor2 = "red";

  const handlebtnS3 = () => {
    closeModal()
  };

  const handlebtnS4 = () => {
    closeModal()
  };
</script>

<h1 class="text-3xl w-full dark:text-white py-8">Small Modals</h1>

<h2 class="text-2xl w-full dark:text-white py-8">Set up</h2>

<p class="dark:text-white py-4 text-lg">Import SmallModal, ModalButton, modalIdStor components and set variables in the script tag. Add `closeModal` method if you want to close the modal in a button.</p>

```html
<script>
  import { SmallModal, ModalButton, modalIdStore } from "flowbite-svelte";
  import { goto } from "$app/navigation";

  const closeModal = () => {
    modalIdStore.update((value) => {
      value = null;
    });
  };

  // for basic
  const idBasic = "basic-modal";
  const btnBasicName = "Basic Modal";

  // for small modal 1
  const btnName1 = "Small Modal";
  const id1 = "small-modal";
  const btnColor1 = "purple";

  const handlebtnS1 = () => {
    closeModal()
    goto("/about");
  };

  const handlebtnS2 = () => {
    closeModal()
  };

  // for small modal 2
  const btnName2 = "Small Modal 2";
  const id2 = "small-modal-2";
  const btnColor2 = "red";

  const handlebtnS3 = () => {
    closeModal()
  };

  const handlebtnS4 = () => {
    closeModal()
  };
</script>
```

<h2 class="text-2xl w-full dark:text-white py-8">Small Modals</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id={idBasic} btnName={btnBasicName} />
</div>

<p class="dark:text-white py-4 text-lg">Create a button and modal.</p>

```html
<ModalButton id={idBasic} btnName={btnBasicName} />
<SmallModal id={idBasic} title="Basic Modal Title">
  Basic Modal Content
</SmallModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Small Modals with Action Buttons</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id={id1} btnName={btnName1} btnColor={btnColor1} />
</div>

```html
<ModalButton id={id2} btnName={btnName2} btnColor={btnColor2} />
<SmallModal
  id={id1}
  btnColor="pink"
  title="Small Modal Title"
  btn1="View"
  btn2="No"
  on:handlebtn1={handlebtnS1}
  on:handlebtn2={handlebtnS2}
>
  Modal 1: Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
</SmallModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Small Modals with different colors</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id={id2} btnName={btnName2} btnColor={btnColor2} />
</div>

```html
<ModalButton id={id2} btnName={btnName2} btnColor={btnColor2} />
<SmallModal
  id={id2}
  btnColor="yellow"
  title="Small Modal Title"
  btn1="Yes"
  btn2="No"
  on:handlebtn1={handlebtnS3}
  on:handlebtn2={handlebtnS4}
>
  Modal 2: Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
</SmallModal>
```

<SmallModal id={idBasic} title="Basic Modal Title">
  Basic Modal Content
</SmallModal>

<SmallModal
  id={id1}
  btnColor="pink"
  title="Small Modal Title"
  btn1="View"
  btn2="No"
  on:handlebtn1={handlebtnS1}
  on:handlebtn2={handlebtnS2}
>
  Modal 1: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
eiusmod tempor incididunt ut labore et dolore magna aliqua.
</SmallModal>

<SmallModal
  id={id2}
  btnColor="yellow"
  title="Small Modal Title"
  btn1="Yes"
  btn2="No"
  on:handlebtn1={handlebtnS3}
  on:handlebtn2={handlebtnS4}
>
  Modal 2: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
  eiusmod tempor incididunt ut labore et dolore magna aliqua.
</SmallModal>

<h2 class="text-2xl w-full dark:text-white py-8">Related components</h2>

<p class="dark:text-white text-lg w-full"><a href="https://flowbite-svelte.vercel.app/modals/small" class="text-blue-600 hover:underline dark:text-blue-500">Small Modal</a></p>

<p class="dark:text-white text-lg w-full"><a href="https://flowbite-svelte.vercel.app/modals/medium" class="text-blue-600 hover:underline dark:text-blue-500">Medium Modal</a></p>

<p class="dark:text-white text-lg w-full"><a href="https://flowbite-svelte.vercel.app/modals/large" class="text-blue-600 hover:underline dark:text-blue-500">Large Modal</a></p>

<p class="dark:text-white text-lg w-full"><a href="https://flowbite-svelte.vercel.app/modals/extra-large" class="text-blue-600 hover:underline dark:text-blue-500">Extra Large Modal</a></p>

<p class="dark:text-white text-lg w-full"><a href="https://flowbite-svelte.vercel.app/modals/signin" class="text-blue-600 hover:underline dark:text-blue-500">Signin Modal</a></p>

<p class="dark:text-white text-lg w-full"><a href="https://flowbite-svelte.vercel.app/modals/all-modals" class="text-blue-600 hover:underline dark:text-blue-500">All Modals</a></p>

<h2 class="text-2xl w-full dark:text-white py-8">References</h2>

<p class="dark:text-white text-lg"><a href="https://flowbite.com/docs/components/modal/" target="_blank" class="text-blue-600 hover:underline dark:text-blue-500">Flowbite Modal</a></p>
