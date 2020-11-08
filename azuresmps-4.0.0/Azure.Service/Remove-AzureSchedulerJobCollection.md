---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076128"
---
# <span data-ttu-id="30ce7-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="30ce7-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="30ce7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="30ce7-103">Удаляет коллекцию заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="30ce7-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="30ce7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30ce7-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30ce7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="30ce7-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30ce7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30ce7-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="30ce7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="30ce7-108">Командлет **Remove-AzureSchedulerJobCollection** удаляет коллекцию заданий планировщика и все задания из этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="30ce7-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="30ce7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30ce7-109">EXAMPLES</span></span>

### <span data-ttu-id="30ce7-110">Пример 1: Удаление коллекции заданий для местоположения</span><span class="sxs-lookup"><span data-stu-id="30ce7-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="30ce7-111">Эта команда удаляет коллекцию заданий планировщика с именем JobCollection01 в расположении для северной центральной точки США.</span><span class="sxs-lookup"><span data-stu-id="30ce7-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="30ce7-112">Команда также удаляет задания в разделе JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="30ce7-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="30ce7-113">Пример 2: Удаление расположения задания</span><span class="sxs-lookup"><span data-stu-id="30ce7-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="30ce7-114">Эта команда удаляет коллекцию заданий планировщика с именем JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="30ce7-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="30ce7-115">Команда также удаляет задания в разделе JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="30ce7-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="30ce7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30ce7-116">PARAMETERS</span></span>

### <span data-ttu-id="30ce7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="30ce7-117">-Force</span></span>
<span data-ttu-id="30ce7-118">Указывает на то, что этот командлет удаляет коллекцию заданий планировщика без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="30ce7-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="30ce7-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="30ce7-119">-JobCollectionName</span></span>
<span data-ttu-id="30ce7-120">Указывает имя удаляемой коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="30ce7-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="30ce7-121">-Location</span><span class="sxs-lookup"><span data-stu-id="30ce7-121">-Location</span></span>
<span data-ttu-id="30ce7-122">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="30ce7-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="30ce7-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="30ce7-123">Valid values are:</span></span> 

- <span data-ttu-id="30ce7-124">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="30ce7-124">Anywhere Asia</span></span>
- <span data-ttu-id="30ce7-125">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="30ce7-125">Anywhere Europe</span></span>
- <span data-ttu-id="30ce7-126">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="30ce7-126">Anywhere US</span></span>
- <span data-ttu-id="30ce7-127">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="30ce7-127">East Asia</span></span>
- <span data-ttu-id="30ce7-128">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="30ce7-128">East US</span></span>
- <span data-ttu-id="30ce7-129">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="30ce7-129">North Central US</span></span>
- <span data-ttu-id="30ce7-130">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="30ce7-130">North Europe</span></span>
- <span data-ttu-id="30ce7-131">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="30ce7-131">South Central US</span></span>
- <span data-ttu-id="30ce7-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="30ce7-132">Southeast Asia</span></span>
- <span data-ttu-id="30ce7-133">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="30ce7-133">West Europe</span></span>
- <span data-ttu-id="30ce7-134">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="30ce7-134">West US</span></span>

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

### <span data-ttu-id="30ce7-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="30ce7-135">-Profile</span></span>
<span data-ttu-id="30ce7-136">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="30ce7-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30ce7-137">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30ce7-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30ce7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ce7-138">CommonParameters</span></span>
<span data-ttu-id="30ce7-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30ce7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ce7-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ce7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ce7-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30ce7-141">INPUTS</span></span>

## <span data-ttu-id="30ce7-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30ce7-142">OUTPUTS</span></span>

## <span data-ttu-id="30ce7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="30ce7-143">NOTES</span></span>

## <span data-ttu-id="30ce7-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30ce7-144">RELATED LINKS</span></span>

[<span data-ttu-id="30ce7-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="30ce7-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="30ce7-146">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="30ce7-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="30ce7-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="30ce7-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


