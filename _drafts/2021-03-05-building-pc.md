---
layout: post
title: Lessons from building (someone else's) computer
date: 2021-03-05
summary: My experiences building a desktop workstation, for use as a deep learning development machine and deployment server. I also list useful resources I used in the process.
categories: general
---

About a month into my machine learning journey, a friend and I wanted to stop paying tithes to Google and Amazon (damn, those data centre GPUs are expensive!), and decided to build a workstation to train and deploy our machine learning models. As a chemist who recently started learning Python and chasing the deep learning fad, the panoply of resources available on the Internet for building a computer was nothing short of confusing.

Initially, I was presented with a nice spreadsheet of parts taken from someone else's website detailing a build for an ML dev machine. I glanced haltingly at the rows and columns, and to my surprise, the estimated cost of the machine would be $5000. What a scam! This was far too costly for an undergraduate. Here's what I did instead:

- List what I need
- Find a bunch of brands online, and figure out what's considered affordable
- Decide if opting for a cheaper option has acceptable downsides

Looking at different options online made me realize one thing: there is probably another brand you've never heard of in the market that is willing to sell you the same thing for a cheaper price. Doing your homework can help you save a small fortune ($1700 in my case). I realized my surprisingly marginalist approach towards cost-benefit analysis probably came from the economics classes I took a few years ago. At least I can now say I learnt something useful in school, I guess.

Below, I expound the lessons I've learnt from this nerve-wracking experience, and I provide a list of useful resources that have helped with cost analysis and shaped my decision-making.

---

**Don't blindly follow a single source of information.** A computer is an investment into your workflow that will last half a decade or more. It is the single most machine that will determine how productive you are as a researcher and developer. Needless to say, there are different horses for different courses; someone else's build will take into account *their* usage needs and budget. Not yours.

**Establish what are the your non-negotiables, and work from there.** For example, if you are doing a machine learning setup, a GPU is crucial. Hence, you wouldn't be stupid to fit a GeForce RTX 2080 Ti, which is Nvidia's top-of-the-line. Though it costs $1700, such expenses can't be helped.

**For other parts, determine what you really need.** You don't need the best CPU for a build that is meant to excel at GPU-intensive workflows. Other than running data preprocessing code and general workloads for everyday computing tasks, your CPU shuttles data from system RAM into the dedicated RAM inside your graphics card. Realistically speaking, you only need *two cores and four threads* per GPU. Any additional increment to the number of cores your CPU has will only provide marginal advances in performance at best.

The same could be said for storage solutions. You would need a decently-sized SSD as a boot disk, to store your OS, swap and system files. Storing applications on it will also provide a noticeable increase in latency and responsiveness, which will eventually pay handsome dividends in productivity.

Purchasing another HDD to store datasets is a good idea. Logically, Disk I/O speeds are not that important in machine learning, as your dataset will be floated in your GPU's RAM during training. It is more important to understand your hardware and set up a pipeline which conducts costly disk I/O operations to transfer your dataset from storage to system RAM for preprocessing while training on the previous minibatch is still ongoing.

**Then, optimize for cost.** You do not need a Samsung SSD that costs $220. Especially for storage components, it is very easy to calculate for and optimize cents per GB. Often, big brands come with high costs and flashy marketing with minimal real effect on your performance. I decided on a Taiwanese brand that provided $0.12/GB, compared to pricier alternatives ($0.18, $0.22 per GB) from industry stalwarts such as Samsung and HP. Ideally, you would compare key performance metrics such as read/write speeds and mean time before failure (MTBF) to evaluate if the savings come with acceptable drawbacks for performance-critical stuff.

**You (probably) don't need a water cooler for your GPU.** If you're planning a build with one or two GPUs, you probably can spare the expense and trouble assembling a water cooling system. Just make sure your GPU fans aren't blowing hot air back into your case — or worse, into another GPU.

**You don't need RGB RAM.** We all know that adding bright flashing lights to your RAM sticks will increase memory performance by 10-15%, a nontrivial amount! (Just kidding, seriously don't waste your money here. You can buy yourself an ice-cream instead.)

**In summary, think before buying!** You are better off not following someone else's build, and you will be better off if you consider your usage and consider other, more inexpensive brands that offer more value for money. 

- List what you need
- Find a bunch of brands online, and figure out what's considered cheap
- Decide if opting for a cheaper option has acceptable

## Resources

- [Anandtech](https://www.anandtech.com/) offers reasonable reviews with comprehensive benchmarking, and includes a number of very helpful buying guides to orientate you about what's available on the market.
- [Tom's Hardware](https://www.tomshardware.com/) is another helpful review website.
- [PCPartPicker](https://pcpartpicker.com/) is good explore different parts in a modular fashion, and compare what you're planning to get with what others in the community have configured.
- [Logical Increments](https://www.logicalincrements.com/) is a great tool to help you rationalise the costs associated with upgrading and downgrading the parts that you have chosen.
- [Tim Dettmers](https://timdettmers.com/2018/12/16/deep-learning-hardware-guide/) offers great advice for ML devs who are just starting out building their own computer.

Maybe, when I do build my own PC one day, I will have many more authoritative things to say about this topic. Until then, that's all I have.