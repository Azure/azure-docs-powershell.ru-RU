---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075482"
---
# <span data-ttu-id="d1e22-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d1e22-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="d1e22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1e22-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e22-103">Удаление существующего веб-задания для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="d1e22-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="d1e22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1e22-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d1e22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1e22-105">DESCRIPTION</span></span>
<span data-ttu-id="d1e22-106">Удаление существующего веб-задания для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="d1e22-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="d1e22-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1e22-107">EXAMPLES</span></span>

### <span data-ttu-id="d1e22-108">Пример 1: удаление существующего веб-задания для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="d1e22-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="d1e22-109">Удаление веб-задания с именем MyWebJob для MyWebSite.</span><span class="sxs-lookup"><span data-stu-id="d1e22-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="d1e22-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1e22-110">PARAMETERS</span></span>

### <span data-ttu-id="d1e22-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d1e22-111">-Force</span></span>
<span data-ttu-id="d1e22-112">Указывает на то, что этот командлет удаляет веб-задание без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d1e22-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d1e22-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d1e22-113">-JobName</span></span>
<span data-ttu-id="d1e22-114">Имя веб-задания.</span><span class="sxs-lookup"><span data-stu-id="d1e22-114">The web job name.</span></span>

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

### <span data-ttu-id="d1e22-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="d1e22-115">-JobType</span></span>
<span data-ttu-id="d1e22-116">Тип веб-задания.</span><span class="sxs-lookup"><span data-stu-id="d1e22-116">The web job type.</span></span>
<span data-ttu-id="d1e22-117">Может инициироваться или непрерывно.</span><span class="sxs-lookup"><span data-stu-id="d1e22-117">Can be triggered or continuous.</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e22-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1e22-118">-Name</span></span>
<span data-ttu-id="d1e22-119">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="d1e22-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="d1e22-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="d1e22-120">-Profile</span></span>
<span data-ttu-id="d1e22-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d1e22-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1e22-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d1e22-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1e22-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="d1e22-123">-Slot</span></span>
<span data-ttu-id="d1e22-124">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="d1e22-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="d1e22-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e22-125">CommonParameters</span></span>
<span data-ttu-id="d1e22-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1e22-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e22-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1e22-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e22-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1e22-128">INPUTS</span></span>

## <span data-ttu-id="d1e22-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1e22-129">OUTPUTS</span></span>

## <span data-ttu-id="d1e22-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1e22-130">NOTES</span></span>

## <span data-ttu-id="d1e22-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1e22-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1e22-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d1e22-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="d1e22-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d1e22-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="d1e22-134">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d1e22-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="d1e22-135">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d1e22-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="d1e22-136">Остановить-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d1e22-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


