# RLCard Showdown


## Installation
RLCard-Showdown has separated frontend and backend. The frontend is built with React and the backend is based on Django and Flask.
###
安装 node (3.6+) / npm
(参考)[https://developer.aliyun.com/article/760687]

```
sudo apt update
sudo apt install nodejs npm
```

### Prerequisite
To set up the frontend, you should make sure you have [Node.js](https://nodejs.org/) and NPM installed. Normally you just need to manually install Node.js, and the NPM package would be automatically installed together with Node.js for you. Please refer to its official website for installation of Node.js.

You can run the following commands to verify the installation
```
node -v
npm -v
```
For backend, make sure that you have **Python 3.6+** and **pip** installed.

### Install Frontend and Backend
The frontend can be installed with the help of NPM:
```
git clone -b master --single-branch --depth=1 https://github.com/datamllab/rlcard-showdown.git
cd rlcard-showdown
npm install
```
The backend of leaderboard can be installed with
```
pip3 install -r requirements.txt
cd server
python3 manage.py migrate
cd ..
```

### Run RLCard-Showdown
1. Launch the backend of leaderboard with
```
cd server
python3 manage.py runserver
```
2. Download the pre-trained models in [Google Drive](https://drive.google.com/file/d/1zx-20xNBDbCFd8GWhZFUkl07lofbNHpy/view?usp=sharing) or [百度网盘](https://pan.baidu.com/s/12MgxVBBz4mgitT74quSWfw) 提取码: qh6s. Extract it in `pve_server/pretrained`.

In a new terminal, start the PvE server (i.e., human vs AI) of DouZero with
```
cd pve_server
python3 run_douzero.py
```
Alternatively, you can start the PvE server interfaced with RLCard:
```
cd pve_server
python3 run_dmc.py
```
They are conceptually the same with minor differences in state representation and training time of the pre-trained models (DouZero is fully trained with more than a month, while DMC in RLCard is only trained for hours).

3. Run the following command in another new terminal under the project folder to start frontend:
```
npm start
```
You can view leaderboard at [http://127.0.0.1:3000/](http://127.0.0.1:3000/) and PvE demo of Dou Dizhu at [http://127.0.0.1:3000/pve/doudizhu-demo](http://127.0.0.1:3000/pve/doudizhu-demo). The backend of leaderboard will run in [http://127.0.0.1:8000/](http://127.0.0.1:8000/). The PvE backend will run in [http://127.0.0.1:5000/](http://127.0.0.1:5000/).

## Demos
![leaderboards](https://github.com/datamllab/rlcard-showdown/blob/master/docs/imgs/leaderboards.png?raw=true)
![upload](https://github.com/datamllab/rlcard-showdown/blob/master/docs/imgs/upload.png?raw=true)
![doudizhu-replay](https://github.com/datamllab/rlcard-showdown/blob/master/docs/imgs/doudizhu-replay.png?raw=true)
![leduc-replay](https://github.com/datamllab/rlcard-showdown/blob/master/docs/imgs/leduc-replay.png?raw=true)

## Contact Us
If you have any questions or feedback, feel free to drop an email to [Songyi Huang](https://github.com/hsywhu) for the frontend or [Daochen Zha](https://github.com/daochenzha) for backend.

## Acknowledgements
We would like to thank JJ World Network Technology Co., LTD for the generous support, [Chieh-An Tsai](https://anntsai.myportfolio.com/) for user interface design, and [Lei Pan](https://github.com/lpan18) for the help in visualizations.




