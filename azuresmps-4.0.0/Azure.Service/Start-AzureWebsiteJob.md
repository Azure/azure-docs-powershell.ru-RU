---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075767"
---
# <span data-ttu-id="e0154-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e0154-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="e0154-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0154-102">SYNOPSIS</span></span>
<span data-ttu-id="e0154-103">Запуск веб-задания для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e0154-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="e0154-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0154-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0154-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0154-105">DESCRIPTION</span></span>
<span data-ttu-id="e0154-106">Командлет **Start-AzureWebsiteJob** запускает веб-задание для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e0154-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="e0154-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0154-107">EXAMPLES</span></span>

### <span data-ttu-id="e0154-108">Пример 1: запуск веб-задания для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="e0154-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="e0154-109">Запуск веб-задания с именем MyWebJob для MyWebSite.</span><span class="sxs-lookup"><span data-stu-id="e0154-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="e0154-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0154-110">PARAMETERS</span></span>

### <span data-ttu-id="e0154-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="e0154-111">-JobName</span></span>
<span data-ttu-id="e0154-112">Имя веб-задания.</span><span class="sxs-lookup"><span data-stu-id="e0154-112">The web job name.</span></span>

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

### <span data-ttu-id="e0154-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="e0154-113">-JobType</span></span>
<span data-ttu-id="e0154-114">Тип веб-задания.</span><span class="sxs-lookup"><span data-stu-id="e0154-114">The web job type.</span></span>
<span data-ttu-id="e0154-115">Может инициироваться или непрерывно.</span><span class="sxs-lookup"><span data-stu-id="e0154-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="e0154-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0154-116">-Name</span></span>
<span data-ttu-id="e0154-117">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="e0154-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="e0154-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0154-118">-PassThru</span></span>
<span data-ttu-id="e0154-119">Возвращает логическое значение, указывающее, что задание успешно запущено.</span><span class="sxs-lookup"><span data-stu-id="e0154-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="e0154-120">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0154-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="e0154-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0154-121">-Profile</span></span>
<span data-ttu-id="e0154-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e0154-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0154-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0154-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0154-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="e0154-124">-Slot</span></span>
<span data-ttu-id="e0154-125">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="e0154-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="e0154-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0154-126">CommonParameters</span></span>
<span data-ttu-id="e0154-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0154-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0154-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0154-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0154-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0154-129">INPUTS</span></span>

## <span data-ttu-id="e0154-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0154-130">OUTPUTS</span></span>

## <span data-ttu-id="e0154-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0154-131">NOTES</span></span>

## <span data-ttu-id="e0154-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0154-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0154-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e0154-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="e0154-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e0154-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="e0154-135">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e0154-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="e0154-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e0154-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="e0154-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e0154-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


