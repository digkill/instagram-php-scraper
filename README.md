# instagram-php-scraper
# Usage

`composer require raiym/instagram-php-scraper`


```php
use InstagramScraper\InstagramScraper;

$instagram = new InstagramScraper();
$account = $instagram->getAccount('kevin');
/*
Available properties: 
    $username;
    $followsCount;
    $followedByCount;
    $profilePicUrl;
    $id;
    $biography;
    $fullName;
    $mediaCount;
    $isPrivate;
    $externalUrl;
*/
echo $account->followedByCount;

$medias = $instagram->getMedias('kevin', 150);

/*
Available properties: 
    $id;
    $createdTime;
    $type;
    $link;
    $imageLowResolutionUrl;
    $imageThumbnailUrl;
    $imageStandardResolutionUrl;
    $imageHighResolutionUrl;
    $caption;
    $videoLowResolutionUrl;
    $videoStandardResolutionUrl;
    $videoLowBandwidthUrl;
*/
echo $medias[0]->imageHighResolutionUrl;
echo $medias[0]->caption;
```