---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076374"
---
# <span data-ttu-id="6cdf0-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="6cdf0-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="6cdf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdf0-103">Включает отладку веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-103">Enables the website's debug.</span></span>

## <span data-ttu-id="6cdf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cdf0-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6cdf0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-105">DESCRIPTION</span></span>
<span data-ttu-id="6cdf0-106">Включает функцию отладки на веб-сайте в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="6cdf0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-107">EXAMPLES</span></span>

### <span data-ttu-id="6cdf0-108">Включение отладки Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="6cdf0-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="6cdf0-109">Включает отладку в VS 2013.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="6cdf0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-110">PARAMETERS</span></span>

### <span data-ttu-id="6cdf0-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cdf0-111">-Name</span></span>
<span data-ttu-id="6cdf0-112">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="6cdf0-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cdf0-113">-PassThru</span></span>
<span data-ttu-id="6cdf0-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6cdf0-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6cdf0-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="6cdf0-116">-Profile</span></span>
<span data-ttu-id="6cdf0-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6cdf0-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6cdf0-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6cdf0-119">-Slot</span></span>
<span data-ttu-id="6cdf0-120">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="6cdf0-121">-Version</span><span class="sxs-lookup"><span data-stu-id="6cdf0-121">-Version</span></span>
<span data-ttu-id="6cdf0-122">Версия Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-122">The Visual Studio version.</span></span>

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

### <span data-ttu-id="6cdf0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdf0-123">CommonParameters</span></span>
<span data-ttu-id="6cdf0-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdf0-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cdf0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdf0-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cdf0-126">INPUTS</span></span>

## <span data-ttu-id="6cdf0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-127">OUTPUTS</span></span>

## <span data-ttu-id="6cdf0-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cdf0-128">NOTES</span></span>

## <span data-ttu-id="6cdf0-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-129">RELATED LINKS</span></span>

[<span data-ttu-id="6cdf0-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="6cdf0-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="6cdf0-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cdf0-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6cdf0-132">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cdf0-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6cdf0-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cdf0-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6cdf0-134">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cdf0-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


