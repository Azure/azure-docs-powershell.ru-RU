---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075819"
---
# <span data-ttu-id="2111a-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2111a-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="2111a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2111a-102">SYNOPSIS</span></span>
<span data-ttu-id="2111a-103">Настройка расположения по умолчанию, подписки, слота и учетной записи хранения для текущей службы.</span><span class="sxs-lookup"><span data-stu-id="2111a-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="2111a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2111a-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2111a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2111a-105">DESCRIPTION</span></span>
<span data-ttu-id="2111a-106">Командлет **Set-AzureServiceProject** задает расположение для развертывания, слот, учетную запись хранения и подписку на текущую службу.</span><span class="sxs-lookup"><span data-stu-id="2111a-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="2111a-107">Эти значения используются при публикации службы в облаке.</span><span class="sxs-lookup"><span data-stu-id="2111a-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="2111a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2111a-108">EXAMPLES</span></span>

### <span data-ttu-id="2111a-109">Пример 1: основные параметры</span><span class="sxs-lookup"><span data-stu-id="2111a-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="2111a-110">Задает расположение для развертывания службы в регионе "Северный центр США".</span><span class="sxs-lookup"><span data-stu-id="2111a-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="2111a-111">Задает в качестве слота развертывания производственную среду.</span><span class="sxs-lookup"><span data-stu-id="2111a-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="2111a-112">Задает учетную запись хранения, которая будет использоваться для размещения определения службы в myStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2111a-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="2111a-113">Задает подписку, на которой будет размещаться служба в mySubscription.</span><span class="sxs-lookup"><span data-stu-id="2111a-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="2111a-114">Каждый раз, когда служба публикуется в облаке, она будет размещена в центре обработки данных в регионе Северный Central США, она обновит слот развертывания и будет использовать указанную подписку и учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="2111a-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="2111a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2111a-115">PARAMETERS</span></span>

### <span data-ttu-id="2111a-116">-Location</span><span class="sxs-lookup"><span data-stu-id="2111a-116">-Location</span></span>
<span data-ttu-id="2111a-117">Область, в которой будет размещена служба.</span><span class="sxs-lookup"><span data-stu-id="2111a-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="2111a-118">Это значение используется при публикации службы в облаке.</span><span class="sxs-lookup"><span data-stu-id="2111a-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="2111a-119">Возможны следующие значения: везде, где бы вы ни находились, где бы вы ни находились, Восточной Азии, восток США, Северный Центральная США, Южная Европа, Юго-Восточная часть США, Юго-ru.</span><span class="sxs-lookup"><span data-stu-id="2111a-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2111a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2111a-120">-PassThru</span></span>
<span data-ttu-id="2111a-121">Указывает на то, что этот командлет возвращает объект, представляющий элемент, на котором оно работает.</span><span class="sxs-lookup"><span data-stu-id="2111a-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="2111a-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2111a-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2111a-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="2111a-123">-Profile</span></span>
<span data-ttu-id="2111a-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2111a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2111a-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2111a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2111a-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="2111a-126">-Slot</span></span>
<span data-ttu-id="2111a-127">Слот (производственный или промежуточный), в котором будет размещена служба.</span><span class="sxs-lookup"><span data-stu-id="2111a-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="2111a-128">Это значение используется при публикации службы в облаке.</span><span class="sxs-lookup"><span data-stu-id="2111a-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="2111a-129">Возможные значения: "производство", "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="2111a-129">Possible values are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2111a-130">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="2111a-130">-Storage</span></span>
<span data-ttu-id="2111a-131">Учетная запись хранения, которая будет использоваться при загрузке пакета службы в облако.</span><span class="sxs-lookup"><span data-stu-id="2111a-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="2111a-132">Если учетная запись хранения не существует, она будет создана при публикации службы в облаке.</span><span class="sxs-lookup"><span data-stu-id="2111a-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2111a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2111a-133">CommonParameters</span></span>
<span data-ttu-id="2111a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2111a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2111a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2111a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2111a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2111a-136">INPUTS</span></span>

## <span data-ttu-id="2111a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2111a-137">OUTPUTS</span></span>

## <span data-ttu-id="2111a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2111a-138">NOTES</span></span>
* <span data-ttu-id="2111a-139">node-dev, PHP-Dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="2111a-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="2111a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2111a-140">RELATED LINKS</span></span>

[<span data-ttu-id="2111a-141">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2111a-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="2111a-142">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2111a-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="2111a-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="2111a-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


