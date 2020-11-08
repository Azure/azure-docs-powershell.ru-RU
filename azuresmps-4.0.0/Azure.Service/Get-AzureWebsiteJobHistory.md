---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076507"
---
# <span data-ttu-id="92986-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="92986-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="92986-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92986-102">SYNOPSIS</span></span>
<span data-ttu-id="92986-103">Получает журнал веб-заданий.</span><span class="sxs-lookup"><span data-stu-id="92986-103">Gets a web job history.</span></span>

## <span data-ttu-id="92986-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92986-104">SYNTAX</span></span>

### <span data-ttu-id="92986-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="92986-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="92986-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="92986-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="92986-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="92986-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92986-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92986-108">DESCRIPTION</span></span>
<span data-ttu-id="92986-109">Получает журнал веб-заданий.</span><span class="sxs-lookup"><span data-stu-id="92986-109">Gets a web job history.</span></span>

## <span data-ttu-id="92986-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92986-110">EXAMPLES</span></span>

### <span data-ttu-id="92986-111">Пример 1: получение журнала для веб-задания</span><span class="sxs-lookup"><span data-stu-id="92986-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="92986-112">Возвращает полную историю для MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="92986-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="92986-113">Пример 2: Получение последнего запуска для веб-задания</span><span class="sxs-lookup"><span data-stu-id="92986-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="92986-114">Получает последнюю информацию о запуске для MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="92986-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="92986-115">Пример 3: получение определенного запуска для веб-задания</span><span class="sxs-lookup"><span data-stu-id="92986-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="92986-116">Получает все сведения о команде Run с идентификатором 10 для MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="92986-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="92986-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92986-117">PARAMETERS</span></span>

### <span data-ttu-id="92986-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="92986-118">-JobName</span></span>
<span data-ttu-id="92986-119">Имя веб-задания.</span><span class="sxs-lookup"><span data-stu-id="92986-119">The web job name.</span></span>

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

### <span data-ttu-id="92986-120">-Последние</span><span class="sxs-lookup"><span data-stu-id="92986-120">-Latest</span></span>
<span data-ttu-id="92986-121">Если указан, возвращайте последнюю историю выполнения.</span><span class="sxs-lookup"><span data-stu-id="92986-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92986-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92986-122">-Name</span></span>
<span data-ttu-id="92986-123">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="92986-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="92986-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="92986-124">-Profile</span></span>
<span data-ttu-id="92986-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92986-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92986-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92986-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92986-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="92986-127">-RunId</span></span>
<span data-ttu-id="92986-128">Указывает идентификатор журнала выполнения, который вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="92986-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92986-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="92986-129">-Slot</span></span>
<span data-ttu-id="92986-130">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="92986-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="92986-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92986-131">CommonParameters</span></span>
<span data-ttu-id="92986-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92986-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92986-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92986-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92986-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92986-134">INPUTS</span></span>

## <span data-ttu-id="92986-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92986-135">OUTPUTS</span></span>

## <span data-ttu-id="92986-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="92986-136">NOTES</span></span>

## <span data-ttu-id="92986-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92986-137">RELATED LINKS</span></span>

[<span data-ttu-id="92986-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="92986-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="92986-139">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="92986-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="92986-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="92986-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="92986-141">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="92986-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="92986-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="92986-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


