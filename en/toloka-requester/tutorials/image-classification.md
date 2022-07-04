# Image classification

In this tutorial, you will learn how to run image classification in Toloka. We will use a project preset designed specifically for this type of data labeling.

Image classification is a type of data labeling task with a finite number of response options.

Use Toloka to classify a set of images into categories that you define. Tolokers look at the images and choose one of the given categories. After you collect all the labeled images, you can apply your dataset for model training.

## Prerequisites

Before you begin make sure that:

- You are [registered](https://toloka.ai/docs/guide/concepts/access.html) in Toloka as a requester.

- You have [topped up](https://toloka.ai/docs/guide/concepts/refill.html) your Toloka account. If you are unsure about the budget, you can do that later in this tutorial. Toloka will display the budget estimate for your project.

## Choose a preset

We recommend starting with a project preset for easier configuration and better results.

1. Follow [this link](https://toloka.yandex.com/requester/templates?choosedCard=xNnBV641x6Psgaby36Y5), or create a project manually:

   1. In the main menu, choose the **Projects** tab, and click **Create a project**.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/choose-preset-step-1.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/choose-preset-step-1.png" alt="Choose a preset. Step 1" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

   1. Select the **Image classification** preset.

1. Click **Choose preset** in the pop-up tab.

## Create a project

Set up how your tasks will look for Tolokers. Tolokers are people around the world who get paid for completing your tasks.

1. Under **General information**, add the project name and description.

   - **Name to show performers**: In 2-5 words, state the general idea of the project.

   - **Description for performers**: In a couple of sentences, explain what you expect Tolokers to do. This is just an overview. You will write instructions later.

   <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-project-step-1.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-project-step-1.png" alt="Create a project. Step 1" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. In the **Task interface** section, set up what your tasks will look like. This preset has a task template with validation, keyboard shortcuts, and task layout pre-configured.

   {% note info %}

   This tutorial uses [Template Builder](https://toloka.ai/en/docs/template-builder/), but you can use the [HTML/JS/CSS editor](https://toloka.ai/docs/guide/concepts/spec.html) for the same purpose.

   {% endnote %}

   1. Using the **Visual editor**, add your data to the Config section:

      - **Question performers will see in your task**: Write a question that matches the responses Tolokers need to choose from. All tasks in a project use the same question.

      - **Paste link to a sample image**: This image is only used to display the task interface preview on the right.

   1. **Set answer options** is pre-filled with sample answers. Replace the samples with your categories. Note that **Other** and **Error** are separate entities.

      - **Answer option for performers**: This is the label that Tolokers will see. Make sure it is clear and correct.

      - **Name in labeling results**: This is the value you will see in the file with the labeling results.

   1. Raw task data and labeling results are stored in TSV files. The **Data specification** section determines which columns these files might have.

      Click **Show specifications** and check the values:

      - **Input data**: Сolumns in the file with raw task data.

      - **Output data**: Сolumns in the file with labeling results.

      **Input data** and **Output data** [match the task interface](https://toloka.ai/en/docs/template-builder/operations/create-specs) you set up in **Template Builder**. Check that there are fields for all data types you use for your tasks, and for the ones you want to see in the results file.

1. Under **Instructions for performers**, add the instructions Tolokers will see when they start doing your tasks. You can add text, tables, and images to your instructions.

   Check the sample text of the instructions, and update it to fit your project.

   {% note tip %}

   When writing instructions, remember that most performers don’t know anything about your tasks beforehand. Make sure your instructions are as clear as possible, but not too wordy. For successful data labeling, try to strike a balance between covering all the essentials and keeping it short. Learn more in our [knowledge base](https://toloka.ai/knowledgebase/instruction/).

   {% endnote %}

1. To save your data and continue, click **Create a project**.

   <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-project-step-4.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-project-step-4.png" alt="Create a project. Step 4" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

## Create a pool

A _pool_ is a set of tasks sent out to Tolokers at the same time. One project can have many pools. When creating a pool, you set up pricing, audience filters for Tolokers, and quality control.

1. Click **Create new pool**.

1. Under **General information**, set the **Pool name**.

1. Under **Audience**, set up filters to select Tolokers for your pool.

   1. Uncheck **My tasks may contain shocking or pornographic content** if your project has none of those.

   1. To select Tolokers based on their language, location, age, gender, and other parameters, click the **Add filter** button. For example, add the **Languages** filter:

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-pool-step-3.2.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-pool-step-3.2.png" alt="Create a pool. Step 3.2" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

   1. Use the **Speed/quality balance** slider to change the number of Tolokers who can see your tasks. Move the slider to the right to exclude Tolokers with lower ratings from participating in your project.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-pool-step-3.3.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/create-pool-step-3.3.png" alt="Create a pool. Step 3.3" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. Under **Quality control**, the **Image classification** preset has preconfigured quality control rules for more accurate results. In most cases, you can keep them as is:

   - **Fast responses**: This rule filters out Tolokers who complete tasks too fast. The default settings mean that Tolokers are banned from the project for 1 day if they respond to 4 out of 5 tasks in less than 15 seconds.

   - **Majority vote**: This rule accepts the most popular response as the correct one, and allows you to filter out Tolokers who answer incorrectly. The default settings mean that Tolokers who give correct responses to less than 40% of tasks are banned from the project for 1 day. **Accept as majority** set to `2` means that 2 similar responses out of all responses given to a single task will be considered as the correct answer.

1. In **Price**, set up how much a single task will cost for you.

   1. In **Price per task suite**, set the amount of money to pay per task suite done by one Toloker. A task suite is a page with a number of tasks. It can contain one or several tasks. If the tasks are simple, you can add 10-20 tasks per suite.

   1. In the **Overlap** field, define how many Tolokers must do each task. The default value (`3`) means that each task will have 3 responses.

   1. At the bottom of the **Price** section, you see **Price per 1 task**. This is the amount of money paid per task.

1. To save the settings and continue, click **Create pool**.

## Upload data

At this step, upload your task data to Toloka.

1. Create a TSV file with tasks.

   1. For this type of task, your TSV file must have one column. Set the header of the column equal to `INPUT:image`.

   1. Add links to your images to the TSV file.

   ```plaintext
   INPUT:image
   https://tlk.s3.yandex.net/dataset/cats_vs_dogs/dogs/041adb571f4342e7a42e47712f492101.jpg
   https://tlk.s3.yandex.net/dataset/cats_vs_dogs/dogs/048e5760fc5a46faa434922b2447a527.jpg
   https://tlk.s3.yandex.net/dataset/cats_vs_dogs/dogs/05334365c060421ab25264166bbb4fd1.jpg
   ```

   {% note tip %}

   To see what a file with tasks looks like, download a sample file by clicking **Template for general tasks.tsv**.

   {% endnote %}

1. Upload your file.

   1. Click **Upload**.

   1. In the **File upload settings** window, define how many tasks will be shown on a single page. Choose **Smart mixing** and specify the following options:

      - **General tasks**: These are the tasks for Tolokers to label.
      - **Training tasks**: These are tasks with predefined answers and explanations for Tolokers.
      - **Control tasks**: These are tasks with predefined answers used to control the quality of responses.

      For example, you can add 9 general tasks and 1 control task per page:

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-2.2.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-2.2.png" alt="Upload your file. Step 2.2" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:450px;" /></a>

   1. Click **Upload**, select your file, wait for the uploading to finish, and click **Add**.

1. To create control tasks, add correct answers to several tasks.

   1. Click **Edit**.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.1.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.1.png" alt="Upload your file. Step 3.1" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

   1. On the **Edit tasks page**, click **Create control tasks**.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.2.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.2.png" alt="Upload your file. Step 3.2" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

   1. Check the **result** checkbox, and select the correct answer for a task. Then, click the **Save and go to next** button. Add several control tasks this way.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.3.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.3.png" alt="Upload your file. Step 3.3" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

      {% note tip %}

      For large pools (over 1000 tasks), we recommend adding at least 1% of control tasks to the pool. For small pools (around 100 tasks), you need 10% control tasks.

      {% endnote %}

   1. Note the **Distribution of correct responses for control tasks** graph on the right side of the page. It shows how many control tasks of each type you have. We recommend adding an equal quantity of each correct response.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.4.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.4.png" alt="[![Upload your file. Step 3.4" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:420px;" /></a>

   1. When you are done adding control tasks, click the pool name in the menu.

      <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.5.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/upload-data-step-3.5.png" alt="Upload your file. Step 3.5" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

## Start labeling

1. Make sure you have [topped up your account](https://toloka.ai/docs/guide/concepts/refill.html).

1. To send the tasks to Tolokers and begin the labeling process, click **Start labeling**.

   <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/start-labeling-step-2.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/start-labeling-step-2.png" alt="Start labeling. Step 2" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. In the pop-up panel, review the budget and click **Launch**.

## See the results

1. You can see the labeling progress on the pool page. Wait until the labeling is completed. Refresh the page to check the progress.

   <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/see-results-step-1.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/see-results-step-1.png" alt="See the results. Step 1" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. When the labeling is complete, click the arrow next to the **Download results** button and choose **Run Dawid-Skene model** from the drop-down menu. Click **Yes** in the pop-up window.

   <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/see-results-step-2.png"><img src="https://yastatic.net/s3/doc-binary/src/toloka/en/guide/tutorials/image-classification/see-results-step-2.png" alt="See the results. Step 2" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. Open the same drop-down menu again, and click **View aggregations list**.

1. Wait until the aggregation is complete, and click **Download**. You will get TSV files with the labeling results:

   - **INPUT**: The data you uploaded for labeling.
   - **OUTPUT**: The results of labeling (category picked by Tolokers).
   - **CONFIDENCE**: The response significance according to the [Dawid-Skene model](https://toloka.ai/docs/guide/concepts/result-aggregation.html#aggr__dawid-skene).

## See also

- [Instructions](https://toloka.ai/knowledgebase/instruction/)
- [Quality control](https://toloka.ai/knowledgebase/quality-control/)
- [Pricing](https://toloka.ai/knowledgebase/pricing/)
- [Template Builder — image classification](https://toloka.ai/en/docs/template-builder/templates/image-classification)
- [Toloka-Kit — image classification](https://github.com/Toloka/toloka-kit/blob/main/examples/1.computer_vision/image_classification/image_classification.ipynb)

## Datasets and reference

- [Sample dataset file with tasks](https://tlk.s3.yandex.net/toloka-kit/knowledge-base/catsdogs.tsv)