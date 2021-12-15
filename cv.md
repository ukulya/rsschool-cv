
# Urkuiash Korgonbekova
## Juinior Front End Developer at Optimizer.kg
![urkuiash](https://github.com/ukulya/rsschool-cv-q1/blob/2ae626401a2bd315dea16fc37423f51676159d92/urkuiash.jpg)
* [+996709426433](tel:996709426433)
* [ukulya150992@gmail.com](mailto:ukulya150992@gmail.com)
* Urkuiash(@ukulya) - discord nick name 
* Urkuiash#1483 - discord contact

### About
I love studying - every day I learn something new.I am very accurate in every aspect of my life. I started my journey as a Front End Developer three years ago. I first learned HTML,CSS and basic JS.
Same time I had enrolled in technical college,where I learned basics of SQL,JAVA,C++,C#. After I graduated from programming courses I applied for a job in local company.I successfully passed an interview and a test task and was accepted.Since then I have 
broadened my knowledge in JS and I picked up several frameworks and programing languages such as PHP,REACT,REDUX,MERN,Symphony,Laravel. Mostly my job is to integrate online-stores and info websites using 
Open Cart and Wordpress. But when I have time I like to explore new things in programming. Right now I have enrolled in Android development (Kotlin) course in local IT Academy. My goal is to keep going and never stop at what I am doing.

### Skills 

* JS      
* PHP
* JAVA
* Kotlin
* SQL
* React
* Redux
* MERN
* Laravel
* Symphony
* Android
* Git
* Open Cart
* Wordpress
* Shopify
* REST API

### Code

```
import {useGetCryptosQuery} from "../services/cryptoApi";
import {useEffect, useState} from "react";
import {Card, Col, Input, Row} from "antd";
import {NavLink} from "react-router-dom";
import millify from "millify";

const Cryptocurrencies = ({simplified}) => {
    const count = simplified ? 10 : 50;
    //const count = 10;
    const {data: cryptosList,isFetching} = useGetCryptosQuery(count)
    //console.log(count) // 10
    //console.log(typeof count) // Number
    const [cryptos,setCryptos] = useState([])
    const [searchTerm,setSearchTerm] = useState('')

    useEffect(() => {
        const filteredData = cryptosList?.data?.coins.filter(coin => coin.name.toLowerCase().includes(searchTerm.toLowerCase()))
        setCryptos(filteredData)
    },[cryptosList,searchTerm])

    if (isFetching) return "loading.."

  return(
      <>
          {!simplified &&
          <div className="search-crypto">
              <Input placeholder={'search crypto currency'} onChange={e => setSearchTerm(e.target.value)}/>
          </div>
          }
        <Row gutter={[32,32]} className={'crypto-card-container'}>
            {cryptos?.map(currency=>(
                <Col xs={24} sm={12} lg={6} className={'crypto-card'} key={currency.id}>
                    <NavLink to={`/crypto/${currency.id}`}>
                        <Card title={`${currency.rank}. ${currency.name}`} extra={<img className={'crypto-image'} src={currency.iconUrl} alt={currency.name}/>} hoverable>
                            <p>Price: {millify(currency.price)}</p>
                            <p>Market: {millify(currency.marketCap)}</p>
                            <p>Daily change: {millify(currency.price)}</p>
                        </Card>
                    </NavLink>
                </Col>
                ))}
        </Row>
      </>
  )
}
export default Cryptocurrencies;
```

### Work Experience
* Optimizer.kg - Junior Front End Developer - 2019 - Present

### Projects

[almurut.store](https://almurut.store)
* Open Cart 
* Queries to DB
* Customized admin panel as per customer request
* PHP,JS,SQL

[moto.optimizer.kg](http://moto.optimizer.kg/)
* Wordpress
* Custom fields in admin panel
* PHP,JS

### Education
* 2021 - Ongoing IT Academy - Android Kotlin
* 2021 - Online course - MERN
* 2020 - 2021 Udemy - JS,REACT,REDUX
* 2018 - 2021 College of Economics,Design and IT 
* 2018 - 2019 IT RUN - Front End Development Course

### Languages
* Kyrgyz,Russian - native
* English - B2
* German - A2
