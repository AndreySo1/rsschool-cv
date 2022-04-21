![foto](https://raw.githubusercontent.com/AndreySo1/And-rs/master/CV120.png "info")
# **Andrey Soroko** 
#### QA Engineer / Junior Frontend Developer

---

### **Contact information:**
#### **Location:** Poland, Wroclaw
#### **Phone:** +48 536 159 006
#### **E-mail:** andreyso88@gmail.com
#### **LinkedIn:** [Andrey Soroko](https://www.linkedin.com/in/soroko-andrey88/)

---

## About me
#### Experience in software testing and project support for PHP/JS, have a technical education

---

## Skils
- QA
- HTML/CSS/SCSS
- JS
- SQL
- PHP
- Yii2
- Git

---

## Code example:
#### Test case, for testing framework Codeception:
``` 
<?php

use yii\helpers\Url;

class DeleteCest
{
	public function deleteUpDraft(SmokeTester $I){
		$I->loginGz('etp000442', '11111111');
		$I->amOnPage('/tenders/drafts');
		$I->seeResponseCodeIs(\Codeception\Util\HttpCode::OK);
                $I->seeInTitle('Мои черновики');
                $I->expectTo('see trash buttons');
                $trashLinks = $I->grabMultiple('.btn-xs', 'href');

        if(count($trashLinks)>0){
        	$I->amOnPage($trashLinks[0]);
        	$trashLinksUpdate = $I->grabMultiple('.btn-xs', 'href');
        	((count($trashLinksUpdate)+1) == count($trashLinks)) ? $I->expect('operation success') : $I->expect('NOT delete');
        	$I->see('Закупка успешно удалена', '#w9-success-0');  
        } else{
        	$I->expect('user not have drafts');
        	$I->see('Нет данных для отображения', '.alert-warning');
        };

	}
} 
```

---

## Experience
#### Providing technical support to company employees (deploying an operation system, installing the software, updating software, connecting peripheral equipment, upgrading / repairing work equipment), remote assistance to customers (installing / configuring specialized software).

---

## Education
#### **Belarusian State University of Informatics and Radioelectronics**
Bachelor's degree: Computer and Information Sciences and Support Services

---

## English
#### A2

