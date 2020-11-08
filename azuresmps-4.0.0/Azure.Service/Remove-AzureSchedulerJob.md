---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076129"
---
# <span data-ttu-id="8b5c2-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="8b5c2-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="8b5c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5c2-103">Удаление задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="8b5c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b5c2-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8b5c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b5c2-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5c2-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8b5c2-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8b5c2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8b5c2-108">Командлет **Remove-AzureSchedulerJob** удаляет задание планировщика.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="8b5c2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b5c2-109">EXAMPLES</span></span>

### <span data-ttu-id="8b5c2-110">Пример 1: удаление задания планировщика</span><span class="sxs-lookup"><span data-stu-id="8b5c2-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="8b5c2-111">Эта команда удаляет задание с именем Job17.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="8b5c2-112">Это задание входит в коллекцию заданий с именем JobCollection01 и находится в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="8b5c2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b5c2-113">PARAMETERS</span></span>

### <span data-ttu-id="8b5c2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8b5c2-114">-Force</span></span>
<span data-ttu-id="8b5c2-115">Указывает на то, что этот командлет удаляет задание планировщика без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8b5c2-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b5c2-116">-JobCollectionName</span></span>
<span data-ttu-id="8b5c2-117">Указывает имя коллекции, содержащей задание планировщика, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="8b5c2-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="8b5c2-118">-JobName</span></span>
<span data-ttu-id="8b5c2-119">Указывает имя задания планировщика, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="8b5c2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="8b5c2-120">-Location</span></span>
<span data-ttu-id="8b5c2-121">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="8b5c2-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8b5c2-122">Valid values are:</span></span> 

- <span data-ttu-id="8b5c2-123">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="8b5c2-123">Anywhere Asia</span></span>
- <span data-ttu-id="8b5c2-124">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="8b5c2-124">Anywhere Europe</span></span>
- <span data-ttu-id="8b5c2-125">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="8b5c2-125">Anywhere US</span></span>
- <span data-ttu-id="8b5c2-126">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="8b5c2-126">East Asia</span></span>
- <span data-ttu-id="8b5c2-127">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="8b5c2-127">East US</span></span>
- <span data-ttu-id="8b5c2-128">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="8b5c2-128">North Central US</span></span>
- <span data-ttu-id="8b5c2-129">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="8b5c2-129">North Europe</span></span>
- <span data-ttu-id="8b5c2-130">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="8b5c2-130">South Central US</span></span>
- <span data-ttu-id="8b5c2-131">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="8b5c2-131">Southeast Asia</span></span>
- <span data-ttu-id="8b5c2-132">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="8b5c2-132">West Europe</span></span>
- <span data-ttu-id="8b5c2-133">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="8b5c2-133">West US</span></span>

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

### <span data-ttu-id="8b5c2-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="8b5c2-134">-Profile</span></span>
<span data-ttu-id="8b5c2-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b5c2-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b5c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5c2-137">CommonParameters</span></span>
<span data-ttu-id="8b5c2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b5c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5c2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5c2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5c2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b5c2-140">INPUTS</span></span>

## <span data-ttu-id="8b5c2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b5c2-141">OUTPUTS</span></span>

## <span data-ttu-id="8b5c2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b5c2-142">NOTES</span></span>

## <span data-ttu-id="8b5c2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b5c2-143">RELATED LINKS</span></span>

[<span data-ttu-id="8b5c2-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="8b5c2-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


