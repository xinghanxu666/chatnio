<div align="center">

![chatnio](/app/public/logo.png)

# [Chat Nio](https://chatnio.net)

_🚀 **下一代 AI 一站式解决方案**_

_🚀 **Next Generation AI One-Stop Solution**_

English | [简体中文](https://github.com/Deeptrain-Community/chatnio/blob/master/README_zh-CN.md)

[Official Website](https://chatnio.net) | [Docs](https://docs.chatnio.net) | [SDKs](https://docs.chatnio.net/developers/sdk) | [QQ Group](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=1mv1Y8SyxnQVvQCoqhmIgVTbwQmkNmvQ&authKey=5KUA9nJPR29nQwjbsYNknN2Fj6cKePkRes%2B1QZy84Dr4GHYVzcvb0yklxiMMNVJN&noverify=0&group_code=749482576)

[![Chat Nio: #1 Repo Of The Day](https://trendshift.io/api/badge/repositories/6369)](https://trendshift.io/repositories/6369)

[![code-stats](https://stats.deeptrain.net/repo/Deeptrain-Community/chatnio)](https://stats.deeptrain.net)

</div>

## 📝 Features

- ✨ **AI Chat Conversation**
  1. **Rich Format Compatibility**
     - Supports Vision models, including ***direct image upload*** and ***image direct link or Base64 image input*** functions (like GPT-4 Vision Preview, Gemini Pro Vision, etc.)
     - Supports drawing with DALL-E models
     - Supports **Imagine** / **Upscale** / **Variant** / **Reroll** operations for Midjourney / Niji models
     ![Midjourney](/screenshot/code.png)
  2. **Markdown Support / Theme Switching Support**, supports light and dark modes, code highlighting, Mermaid, LaTeX formulas, tables, progress bars, Virtual Message, etc.
     ![Markdown Message](/screenshot/latex.jpg)
     ![Markdown Mermaid](/screenshot/mermaid.png)
  3. **Support for Message Menu**, including re-answering, copying messages, using messages, editing messages, deleting messages, saving as a file, and more operations...
     ![Vision Support](/screenshot/vision.png)
  4. **Support for Multi-platform Adaptation**, supports PWA apps, desktop platforms (desktop is based on [Tauri](https://github.com/tauri-apps/tauri)).
  5. **Dialogue Memory**, cloud synchronization, native support for direct link sharing of site conversations, supports using shared conversations, saving shared conversations as images, and share management (including viewing, deleting shares, etc.).
     ![Conversation Sharing](/screenshot/sharing.png)
  6. **Native Support for Full Model File Parsing**, supports pdf, docx, pptx, xlsx, images, and other formats parsing (for more details, see the project [chatnio-blob-service](https://github.com/Deeptrain-Community/chatnio-blob-service)).
     ![File Upload](/screenshot/file.png)
  7. Supports Full-model DuckDuckGo Online Search _(for details, refer to the [duckduckgo-api](https://github.com/binjie09/duckduckgo-api) project, needs to be set up on your own and configured in the internet settings in the system settings, thanks to the author [@binjie09](https://github.com/binjie09), enable web searching by prefixing the relay api model with **web-**.)_
     ![Online Search](/screenshot/online.png)
  8. **Full-screen Large Text Editing**, supports *plain text editing*, *edit-preview mode*, *pure preview mode* three mode switching.
     ![Editor](/screenshot/editor.png)
  9. **Model Marketplace**, supports model search, supports drag-and-drop in sequence, includes model name, model description, model Tags, model avatar, automatic binding of model pricing, automatic binding of subscription quotas (models included in the subscription will be tagged with *plus* label)
     ![Model Market](/screenshot/market.png)
  10. **Support for Preset**, supports ***custom presets*** and **_cloud synchronization_** features, supports preset cloning, preset avatar settings, preset introduction settings
    ![Preset Settings](/screenshot/mask.png)
    ![Preset Editing](/screenshot/mask-editor.png)
  11. **Support for Site Announcements** Supports site announcements and notifications
  12. **Support for Preference Settings**, i18n multi-language support, custom maximum number of carry-over sessions, maximum reply tokens number, model parameters customization, reset settings, etc.
    ![Preference Settings](/screenshot/settings.png)
  13. **Internationalization Support**, support multi-language switching
  14. **Additional** _(User group permissions for additional functions can be enabled and disabled through backend system settings)_
    - *[Discontinued]* 🍎 **AI project generator function**, supports viewing of the generation process, supports TAR / ZIP format downloads *(based on presets, may be unstable)*
    - *[Discontinued]* 📂 **Bulk article generation function**, supports progress bar, one-click generation of DOCX documents in TAR / ZIP format download *(requires a generation quantity higher than the highest concurrency number of the upstream model)*
    - *[Deprecated]* 🥪 **AI Card feature** (deprecated), AI questions and answers are presented in the form of cards, can be directly embedded via image url. *(Based on dynamic SVG generation)*
- 🔔 **Rich Admin System**
    1. **Rich and beautiful dashboard**, including current day and month's crediting information, subscribers, model usage statistics line charts, pie charts, revenue statistics, user type statistics, model usage statistics, request counts and model error counts statistics charts, etc.
       ![Dashboard](/screenshot/admin.png)
    2. **Support user management**, *User list*, *User details*, *Administrative operations* (*Change password*, *Change mailbox*, *Block/Unblock user*, *Set as administrator*, *Points change*, *Points setup*, *Subscription management*, *Subscription level setup*, *Release subscription*, etc).
    3. **Support Gift Code and Redemption Code Management** Support management operations, support batch generation and save to file.
    4. **Price setting**, support model price setting (_**Counts billing**_, **_Token flexible billing_**, _**No billing**_ etc.), support synchronize the price setting of upstream Chat Nio site (optional whether to override the price rules of the existing models on this site), unset price model detection (if non-administrator will automatically detect and stop using the model to prevent loss of money). to prevent loss of money)
       ![Buy Points](/screenshot/shop.png)
       ![Price setting](/screenshot/charge.png) !
    5. **Subscription Settings**, different from flexible billing, subscription is a kind of fixed price per time billing, platform users can subscribe to a fixed price through the package, support whether to enable subscription (default off), support subscription tiering, support subscription quota settings, support subscription quotas cover the model settings, icon settings, quotas imported from other packages and other functions.
       ![Subscription Plan](/screenshot/subscription.png)
       ![Subscription Settings](/screenshot/plan.png) !
    6. **Customize Model Marketplace**, Edit Frontend Model Marketplace Model Name, Description, Tags, Avatar (Built-in Model Image Selection and Custom Model Image Setting), Whether or not to add Model Models and other information!
       ![Model Market Settings](/screenshot/admin-market.png)
    7. **System Settings**, Customized Site Name, Site Logo, Documentation Link, Whether to Suspend Registration, User Initial Points Settings, Customized Purchase Link (Card Address), Contact Information, Footer Information, etc. !
       ![System Settings](/screenshot/system.png)
    8. **SMTP support**, support whether to enable email suffix whitelisting, support customized email suffix whitelisting.
    9. **Support model caching**, *i.e., under the same entry, if it has been requested before, it will return the cached result directly (hit caching will not be billed), to reduce the number of requests. You can customize the maximum number of cached results for a case (default is 1), customize the models that can be cached (default is empty), customize the caching time (default is 1 hour), support one-click settings *All models are not cached*, *Free models are cached*, *All models are cached*, and other operations*.
- ⚡ Channel Management System
  1. Chat Nio **uses a self-developed channel distribution algorithm** (doesn't rely on http context), abstracts Adapter compatibility layer architecture, low coupling, and high scalability.
  2. **Supports Multi-channel Management**, supports **priority allocation**, **weight load**, **channel status management**, etc. _(Priority refers to the allocation of channel priority during the model request process, where higher priority channels are used first. If an error occurs, the system will automatically fall back to a channel of lower priority; weight refers to the weight of a channel within the same priority, with higher weight increasing the probability of being used. For channels at the same priority level, only one can be used at any time, and the higher the weight, the higher the probability of being selected.)_
  3. **Compatible With Multiple Formats**, supports multiple model compatibility layers, see the model support section below for details.
  4. **Supports Custom Models**, allows for the use of known models through *adding models*, supports the addition of custom models, supports one-click filling of template models (referring to the template models supported by the current format by default, such as OpenAI format template models like *gpt-3.5-turbo-0613*), supports one-click clearing of models.
  5. **Supports Channel Retries**, supports a Retry mechanism for channels, allows for custom retry counts, after surpassing the retry count the system will automatically fall.
  6. **Supports Balanced Load Within The Same Channel**, a single channel can be configured with multiple keys instead of creating channels in bulk (multiple keys separated by line breaks), assigning requests with equal weight randomly, and the Retry mechanism will also be used in conjunction with multiple keys within the same channel, randomly selecting keys for retries.
  7. **Supports Channel Model Mapping**, maps models to the models already supported by this channel, format as *target model*>*existing model*, adding a prefix `!` allows existing models not to be allocated in the channel's hit models, for the specific usage method, please refer to the instructions and tips in the channel settings within the program.
  8. **Supports User Grouping**, custom selection of user groups that can use this model (such as _anonymous users_, _regular users_, _basic subscription users_, _standard subscription users_, _professional subscription users_, etc., setting to group 0 available and setting to all groups available are the same effect).
  9. **Built-in Upstream Hiding**, automatically hides the upstream URL set within the channel when an error occurs (e.g., _**channel://2**/v1/chat/completions_), also supports hiding keys (_Gemini, you're really good job_), to prevent upstream channels from being misused in cases where keys are not set or upstream error information exposes the full key (such as reverse-type channels), and also facilitates troubleshooting in cases where multiple channels serve the same access point simultaneously.
  ![Channel Settings](/screenshot/channel.png)
  ![Channel Group](/screenshot/channel-group.png)
- ✨ Forwarding API Services
  1. Compatible with multiple formats in the OpenAI universal format and supporting multiple model compatible layers, this means you can use a format while supporting multiple AI models.
  2. Replace `https://api.openai.com` with `https://api.chatnio.net` (example), enter the API Key from `API Settings` in the console to use, support for resetting Key.
  3. Supported Formats
    - [x] Chat Completions _(/v1/chat/completions)_
    - [x] Image Generation _(/v1/images)_
    - [x] Model List _(/v1/models)_
    - [x] Dashboard Billing _(/v1/billing)_
- 🎃 More features waiting for your discovery...


## 🔨 Supported Models
- [x] OpenAI
  - [x] Chat Completions (support *vision*, *tools_calling* and *function_calling*)
  - [x] Image Generation
- [x] Azure OpenAI
- [x] Anthropic Claude (support *vision*)
- [x] Slack Claude (deprecated)
- [x] Sparkdesk (support *function_calling*)
- [x] Google Gemini (PaLM2)
- [x] New Bing (creative, balanced, precise)
- [x] ChatGLM (turbo, pro, std, lite)
- [x] DashScope Tongyi (plus, turbo)
- [x] Midjourney
    - [x] Mode Toggling (relax, fast, turbo)
    - [x] Support U/V/R Actions
- [x] Tencent Hunyuan
- [x] Baichuan AI
- [x] Moonshot AI
- [x] Groq Cloud AI
- [x] ByteDance Skylark (support *function_calling*)
- [x] 360 GPT
- [x] LocalAI (Stable Diffusion, RWKV, LLaMa 2, Baichuan 7b, Mixtral, ...) _*requires local deployment_


## 📦 Deployment
*Once deployment is successful, the administrator account is `root`, the default password is `chatnio123456`*

1. ⚡ Install with Docker Compose (Recommended)
    
    > The host mapping address is `http://localhost:8000` after successful operation.

    ```shell
    git clone --depth=1 --branch=main --single-branch https://github.com/Deeptrain-Community/chatnio.git
    cd chatnio
    docker-compose up -d # Running the service
   # To use the stable version, replace with `docker-compose -f docker-compose.stable.yaml up -d`.
   # To enable automatic updates with Watchtower, replace with `docker-compose -f docker-compose.watch.yaml up -d`.
    ```
   
   Version Update (_With Watchtower auto-updating enabled, there is no need for manual updates_):
   ```shell
   docker-compose down 
   docker-compose pull
   docker-compose up -d
   ```
   
   > - Mount directory for MySQL database: ~/**db**
   > - Mount directory for Redis database: ~/**redis**
   > - Mount directory for configuration files: ~/**config**

2. ⚡ Docker installation (when running lightweight, it is often used in external _Mysql/RDS_ service)  
    > The host mapping address is `http://localhost:8094` after successful operation. If you need to use the stable version, please use `programzmh/chatnio:stable` instead of `programzmh/chatnio:latest`.  
    ```shell
   docker run -d --name chatnio \
      --network host \
      -v ~/config:/config \
      -v ~/logs:/logs \
      -v ~/storage:/storage \
      -e MYSQL_HOST=localhost \
      -e MYSQL_PORT=3306 \
      -e MYSQL_DB=chatnio \
      -e MYSQL_USER=root \
      -e MYSQL_PASSWORD=chatnio123456 \
      -e REDIS_HOST=localhost \
      -e REDIS_PORT=6379 \
      -e SECRET=secret \
      -e SERVE_STATIC=true \
      programzmh/chatnio:latest
    ```
   > - *--network host* Assigns the container to use the host network, allowing it to access the host's network. You can modify this as needed.
   > - SECRET: JWT Secret Key, generate a random string to modify
   > - SERVE_STATIC: Whether to enable static file service (normally there is no need to change this item, see below for answers to frequently asked questions)
   > - *-v ~/config:/config* mount host machine directory of configuration file, *-v ~/logs:/logs* mount host machine directory of log file,*-v ~/storage:/storage* mount generated files of additional functions
   > - You need to configure MySQL and Redis services, please refer to the information above to modify the environment variables yourself.
    
    Version Update (_With Watchtower auto-updating enabled, there is no need for manual updates, Just run through the steps above again after execution._)：
    ```shell
    docker stop chatnio
    docker rm chatnio
    docker pull programzmh/chatnio:latest
   ```

3. ⚒ Custom Build and Install (Highly Customizable)
    > After deployment, the default port is **8094**, and the access address is `http://localhost:8094`.
    > Configuration options (~/config/**config.yaml**) can be overridden using environment variables, such as the `MYSQL_HOST` environment variable can override the `mysql.host` configuration item.

    ```shell
    git clone https://github.com/Deeptrain-Community/chatnio.git
    cd chatnio
   
    cd app
    npm install -g pnpm
    pnpm install
    pnpm build
   
    cd ..
    go build -o chatnio
   
    nohup ./chatnio > output.log & # using nohup to run in background
    ```

## ❓ Frequently Asked Questions Q&A
1. **Why does my deployed site have access to pages, can sign in, but can't use chat (keeps going in circles)?**
   - Chat and other such features communicate through websockets; please ensure that your server supports websockets. (Tip: Transmission through HTTP can be achieved, without the need for websocket support)
   - If you are using reverse proxies such as Nginx, Apache, please make sure you have configured websocket support.
   - If you are using services like port mapping, port forwarding, CDN, API Gateway, etc., ensure that your service supports and has WebSocket enabled.
2. **My Midjourney Proxy-formatted channel keeps spinning or showing an error message `please provide available notify url`**
   - If it's going around in circles, make sure your Midjourney Proxy service is up and running and that you've configured the correct upstream address.
   - **Midjourney To fill in the channel type, use Midjourney instead of OpenAI (IDK why a lot of people fill in the OpenAI type format and then come back with feedback on why it's an empty response, except for the mj-chat class).**
   - After resolving these issues, please check if the **backend domain** is properly configured in your system settings. If it's not set up, it may prevent the Midjourney Proxy service from functioning correctly.
3. **What external dependencies does this project have?**
   - MySQL: Store persistent data such as user information, chat records, and administrator details.
   - Redis: Storing user quick authentication information, IP rate limits, subscription quotas, email verification codes, etc.
   - If the environment is not properly set up, it may cause the service to fail. Please ensure that your MySQL and Redis services are running smoothly (for Docker deployment, you'll need to set up external services manually).
4. **My server is ARM architecture, does this project support ARM architecture?**
   - Yes. The Chat Nio project uses BuildX to build multi-arch images, so you can run it directly with docker-compose or docker without any additional configuration.
   - If you are using a build installation, you can compile directly on the ARM machine without any additional configuration. If you are compiling on an x86 machine, please use `GOARCH=arm64 go build -o chatnio` for cross-compilation and upload it to the ARM machine for execution.
5. **How do I change the default root password?**
   - Please click on the avatar in the top right corner or the user box at the bottom of the sidebar to go to the backend management, click on the Modify Root Password under the Operation Bar of the General Settings in the System Settings. Alternatively, you can choose to modify the root user's password in the User Management.
6. **What is the backend domain in the System Settings?**
   - The backend domain refers to the address of the backend API service, which is usually the address of the site followed by `/api`, such as `https://example.com/api`.
   - If set to non-*SERVE_STATIC* mode, enabling frontend and backend separation deployment, please set the backend domain to the address of your backend API service, such as `https://api.example.com`.
   - The backend domain is used here for the backend callback address of the Midjourney Proxy service; if you do not need to use the Midjourney Proxy service, please ignore this setting.
7. **How do I configure the payment method?**
   - The Chat Nio open-source version supports the card issuance model; simply set the Purchase Link in the System Settings to your card issuance address. Card codes can be generated in bulk through the Gift Code Management in User Management.
8. **What is the difference between gift codes and redemption codes?**
   - A gift code can only be bound once by a single user, and it is not an aff code or a way to distribute benefits; it can be redeemed from the Gift Code option under the avatar dropdown menu.
   - A redemption code can be bound by