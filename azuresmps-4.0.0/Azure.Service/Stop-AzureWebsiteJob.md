---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075838"
---
# <span data-ttu-id="0af09-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0af09-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="0af09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0af09-102">SYNOPSIS</span></span>
<span data-ttu-id="0af09-103">Остановка веб-задания для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="0af09-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="0af09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0af09-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0af09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0af09-105">DESCRIPTION</span></span>
<span data-ttu-id="0af09-106">Командлет **Stop-AzureWebsiteJob** останавливает веб-задание для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="0af09-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="0af09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0af09-107">EXAMPLES</span></span>

### <span data-ttu-id="0af09-108">Пример 1: остановка веб-задания для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="0af09-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="0af09-109">Останавливает веб-задание с именем MyWebJob для MyWebSite.</span><span class="sxs-lookup"><span data-stu-id="0af09-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="0af09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0af09-110">PARAMETERS</span></span>

### <span data-ttu-id="0af09-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="0af09-111">-JobName</span></span>
<span data-ttu-id="0af09-112">Имя веб-задания.</span><span class="sxs-lookup"><span data-stu-id="0af09-112">The web job name.</span></span>

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

### <span data-ttu-id="0af09-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0af09-113">-Name</span></span>
<span data-ttu-id="0af09-114">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="0af09-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="0af09-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0af09-115">-PassThru</span></span>
<span data-ttu-id="0af09-116">Возвращает логическое значение, указывающее, что задание успешно остановлено.</span><span class="sxs-lookup"><span data-stu-id="0af09-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="0af09-117">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0af09-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="0af09-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="0af09-118">-Profile</span></span>
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

### <span data-ttu-id="0af09-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="0af09-119">-Slot</span></span>
<span data-ttu-id="0af09-120">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="0af09-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="0af09-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af09-121">CommonParameters</span></span>
<span data-ttu-id="0af09-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0af09-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af09-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af09-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af09-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0af09-124">INPUTS</span></span>

## <span data-ttu-id="0af09-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0af09-125">OUTPUTS</span></span>

## <span data-ttu-id="0af09-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0af09-126">NOTES</span></span>

## <span data-ttu-id="0af09-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0af09-127">RELATED LINKS</span></span>

[<span data-ttu-id="0af09-128">Остановить-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0af09-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="0af09-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0af09-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="0af09-130">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0af09-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="0af09-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0af09-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="0af09-132">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0af09-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


