---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075937"
---
# <span data-ttu-id="46fcd-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="46fcd-101">Test-AzureName</span></span>

## <span data-ttu-id="46fcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="46fcd-103">Проверяет, существует ли имя облачной службы Microsoft Azure, имя службы хранилища или имя пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="46fcd-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="46fcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46fcd-104">SYNTAX</span></span>

### <span data-ttu-id="46fcd-105">Сервиса</span><span class="sxs-lookup"><span data-stu-id="46fcd-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="46fcd-106">Склад</span><span class="sxs-lookup"><span data-stu-id="46fcd-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="46fcd-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="46fcd-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="46fcd-108">Веб-сайта</span><span class="sxs-lookup"><span data-stu-id="46fcd-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46fcd-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46fcd-109">DESCRIPTION</span></span>
<span data-ttu-id="46fcd-110">Если имя существует, командлет возвращает $True.</span><span class="sxs-lookup"><span data-stu-id="46fcd-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="46fcd-111">Если имя не существует, оно возвращает $False.</span><span class="sxs-lookup"><span data-stu-id="46fcd-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="46fcd-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46fcd-112">EXAMPLES</span></span>

### <span data-ttu-id="46fcd-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46fcd-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="46fcd-114">Эта команда проверяет, является ли "MyNameService1" существующим именем облачной службы Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46fcd-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="46fcd-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="46fcd-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="46fcd-116">Эта команда проверяет, является ли "mystorename1" существующим именем службы хранилища Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46fcd-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="46fcd-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="46fcd-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="46fcd-118">Эта команда проверяет, является ли "MyNamespace" существующим именем пространства имен служебной шины Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46fcd-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="46fcd-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46fcd-119">PARAMETERS</span></span>

### <span data-ttu-id="46fcd-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46fcd-120">-Name</span></span>
<span data-ttu-id="46fcd-121">Указывает имя службы или учетной записи хранилища для проверки.</span><span class="sxs-lookup"><span data-stu-id="46fcd-121">Specifies the name of the service or storage account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46fcd-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="46fcd-122">-Profile</span></span>
<span data-ttu-id="46fcd-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="46fcd-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46fcd-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46fcd-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46fcd-125">-Служба</span><span class="sxs-lookup"><span data-stu-id="46fcd-125">-Service</span></span>
<span data-ttu-id="46fcd-126">Задает проверку существующей учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="46fcd-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fcd-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="46fcd-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="46fcd-128">Задает проверку пространства имен для существующего Service Bus.</span><span class="sxs-lookup"><span data-stu-id="46fcd-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fcd-129">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="46fcd-129">-Storage</span></span>
<span data-ttu-id="46fcd-130">Определяет проверку существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="46fcd-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fcd-131">-Веб-сайт</span><span class="sxs-lookup"><span data-stu-id="46fcd-131">-Website</span></span>
<span data-ttu-id="46fcd-132">Проверка существующего веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="46fcd-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fcd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fcd-133">CommonParameters</span></span>
<span data-ttu-id="46fcd-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46fcd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fcd-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46fcd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fcd-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46fcd-136">INPUTS</span></span>

## <span data-ttu-id="46fcd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46fcd-137">OUTPUTS</span></span>

## <span data-ttu-id="46fcd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="46fcd-138">NOTES</span></span>
* <span data-ttu-id="46fcd-139">node-dev, PHP-Dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="46fcd-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="46fcd-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46fcd-140">RELATED LINKS</span></span>

