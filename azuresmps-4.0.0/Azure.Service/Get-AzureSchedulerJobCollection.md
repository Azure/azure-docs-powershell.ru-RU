---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075612"
---
# <span data-ttu-id="2db5f-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2db5f-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="2db5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2db5f-102">SYNOPSIS</span></span>
<span data-ttu-id="2db5f-103">Получение коллекций заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="2db5f-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="2db5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2db5f-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2db5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2db5f-105">DESCRIPTION</span></span>
<span data-ttu-id="2db5f-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2db5f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2db5f-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2db5f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2db5f-108">Командлет **Get-AzureSchedulerJobCollection** получает одну или несколько коллекций заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="2db5f-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="2db5f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2db5f-109">EXAMPLES</span></span>

### <span data-ttu-id="2db5f-110">Пример 1: получение всех коллекций</span><span class="sxs-lookup"><span data-stu-id="2db5f-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="2db5f-111">Эта команда получает все коллекции заданий планировщика для всех местоположений в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2db5f-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="2db5f-112">Пример 2: получение всех коллекций для местоположения</span><span class="sxs-lookup"><span data-stu-id="2db5f-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="2db5f-113">Эта команда получает все коллекции заданий планировщика в расположении с названием "Север Central США".</span><span class="sxs-lookup"><span data-stu-id="2db5f-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="2db5f-114">Пример 3: получение коллекции с помощью имени</span><span class="sxs-lookup"><span data-stu-id="2db5f-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="2db5f-115">Эта команда получает коллекцию заданий планировщика с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="2db5f-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="2db5f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2db5f-116">PARAMETERS</span></span>

### <span data-ttu-id="2db5f-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2db5f-117">-JobCollectionName</span></span>
<span data-ttu-id="2db5f-118">Указывает имя коллекции заданий планировщика, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2db5f-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="2db5f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2db5f-119">-Location</span></span>
<span data-ttu-id="2db5f-120">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="2db5f-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="2db5f-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2db5f-121">Valid values are:</span></span> 

- <span data-ttu-id="2db5f-122">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="2db5f-122">Anywhere Asia</span></span>
- <span data-ttu-id="2db5f-123">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="2db5f-123">Anywhere Europe</span></span>
- <span data-ttu-id="2db5f-124">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="2db5f-124">Anywhere US</span></span>
- <span data-ttu-id="2db5f-125">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="2db5f-125">East Asia</span></span>
- <span data-ttu-id="2db5f-126">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="2db5f-126">East US</span></span>
- <span data-ttu-id="2db5f-127">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="2db5f-127">North Central US</span></span>
- <span data-ttu-id="2db5f-128">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="2db5f-128">North Europe</span></span>
- <span data-ttu-id="2db5f-129">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="2db5f-129">South Central US</span></span>
- <span data-ttu-id="2db5f-130">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="2db5f-130">Southeast Asia</span></span>
- <span data-ttu-id="2db5f-131">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="2db5f-131">West Europe</span></span>
- <span data-ttu-id="2db5f-132">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="2db5f-132">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db5f-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="2db5f-133">-Profile</span></span>
<span data-ttu-id="2db5f-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2db5f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2db5f-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2db5f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2db5f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db5f-136">CommonParameters</span></span>
<span data-ttu-id="2db5f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2db5f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db5f-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db5f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db5f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2db5f-139">INPUTS</span></span>

## <span data-ttu-id="2db5f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2db5f-140">OUTPUTS</span></span>

## <span data-ttu-id="2db5f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="2db5f-141">NOTES</span></span>

## <span data-ttu-id="2db5f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2db5f-142">RELATED LINKS</span></span>

[<span data-ttu-id="2db5f-143">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2db5f-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="2db5f-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2db5f-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="2db5f-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2db5f-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


