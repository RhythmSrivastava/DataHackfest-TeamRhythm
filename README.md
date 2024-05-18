<div align="center">
  <img alt="HackRx3.0" src="docs/hackrx.png" height="65" />
</div>
<div align="center">
  <img alt="NudgeLab by NudgeFudge" src="docs/logo.svg" height="56" />
</div>

<br>
<p align="center">
<b>Team NudgeFudge presents NudgeLab.
<br>
No Code App Nudges</b>
</p>
<blockquote align="center"> 
  built on <span style="color: #8b0000;">☕</span> at <a href="https://hackrx.in">HackRx3.0</a>.

</blockquote>

# 💡 Problem Statement

Develop an in-app tool to allow setting up in-app nudges for various use cases, tool to allow nudge configuration on screen without need of having to code them on the screen / per use case.

# 🧠 Knowledge Primer

- A _Nudge_ is a visual element that is used to draw attention of the user to something, for example a new section in an application.
- There are two types of _Users_ that we have considered
  - **Admin**, a kind of user that adds the nudges.
  - **Client** are the ones for which the nudges are created.
- We have considered there are two types of ways to render a nudge
  - **Campaign**s, that can be run manually by _Admin_.
  - **Trigger** based, that are displayed after execution of a particular function, identified via unique `event_label`.
- Our implementation builds upon the existing backend servers of a business. These backends are referred to as **Business Backend**.

# 📺 Preview

<div align="center">
  <img alt="Preview Images" src="docs/preview1.png" />
</div>
<div align="center">
  <img alt="Preview Images" src="docs/preview2.png" />
</div>
<div align="center">
  <img alt="Preview Images" src="docs/preview3.png" />
</div>
<div align="center">
  <img alt="Preview Images" src="docs/preview4.png" />
</div>
<div align="center">
  <img alt="Preview Images" src="docs/preview5.png" />
</div>
<div align="center">
  <img alt="Preview Images" src="docs/preview6.png" />
</div>

# 💻 Tech Stack

- MongoDB
- ExpressJS
- ReactJS
- NodeJS
- TypeScript
- Redis

# 🔧 Utilisation

1. Go to the **[`Admin Dashboard`](https://nudgelab.vercel.app)** and create your project
2. In your project, add some nudges
3. Copy the script tag generated and paste it at the end of your `body` element

```html
<body>
  <!-- your code -->
  <script
    src="https://nudgelab.jagnani73.com/api/v1/nudge/campaign.js"
    data-app-id="demo-app-id"
  ></script>
</body>
```

# 📦 Inside the box

## 1. Importing Data
- Utilized AWS Command Line Interface (CLI) to synchronize data from AWS S3 bucket.
- Command used:
  `aws s3 sync --no-sign-request s3://amazon-last-mile-challenges/almrrc2021/ almrrc2021_data
`
- Ensured the local environment had the necessary AWS CLI tools and permissions configured to access the S3 bucket.


## 2. Cleaning Data

  ###### 1. Data Organization

- Data comprised several JSON files organized into three main directories:
    - `model_apply_inputs`
    - `model_build_inputs`
    - `model_score_inputs`

###### 2. Data Conversion

- Utilized a script to automate the conversion of JSON files to CSV format.
- Ensured that the conversion process retained all relevant data fields and structures.
- Performed data validation checks post-conversion to ensure the integrity and completeness of the data in CSV format.
###### 3. Data Sampling

- Sampled each CSV file to a maximum size of 50MB.
- Applied randomness in the sampling process using a seed set to 1 to ensure reproducibility.

###### 4. DataFrame Creation

- Combined the CSV files within each folder into a unified DataFrame limited to 100MB using pandas.
- Ensured that the DataFrame maintained all necessary attributes and was ready for further analysis or model building.


# ⏭️ What's next

- Add more types of nudges, with more customizing options
- Dynamic drag and drop to get IDs of elements
- Analytics for the nudges and how the user responds to them; tracking user engagement
- Using a DLQ (Dead Letter Queue) for nudges that were not able to be received; cases of failure of delivery
- Adding support for more platforms
- Adding user specific nudges

# 📜 License

`NudgeLab` is available under the MIT license. See the [`LICENSE`](https://github.com/HackRx3/PS1_NudgeFudge/blob/main/LICENSE) file for more info.

# 🤝 Contributing

Please read [`Contributing.md`](https://github.com/HackRx3/PS1_NudgeFudge/blob/main/Contributing.md) for details on our code of conduct, and the process for submitting pull requests to us.

# 💥 Contributors

<a href="https://github.com/RhythmSrivastava/RhygyaHackathon/graphs/contributors">
<img src="https://contrib.rocks/image?repo=RhythmSrivastava/RhygyaHackathon" alt="Contributors">
</a>
                                                                                  
# 🚨 Forking this repo

Many people have contacted us asking if they can use this code for their own websites. The answer to that question is usually "yes", with attribution. There are some cases, such as using this code for a business or something that is greater than a personal project, that we may be less comfortable saying yes to. If in doubt, please don't hesitate to ask us.

We value keeping this site open source, but as you all know, _**plagiarism is bad**_. We spent a non-negligible amount of effort developing, designing, and trying to perfect this iteration of our website, and we are proud of it! All we ask is to not claim this effort as your own.

Refer to this handy [quora post](https://www.quora.com/Is-it-bad-to-copy-other-peoples-code) if you're not sure what to do. Thanks!