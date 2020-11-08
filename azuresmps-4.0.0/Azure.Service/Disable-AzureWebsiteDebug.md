---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075691"
---
# <span data-ttu-id="ca5da-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="ca5da-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="ca5da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca5da-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5da-103">Отключает отладку веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="ca5da-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="ca5da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca5da-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca5da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca5da-105">DESCRIPTION</span></span>
<span data-ttu-id="ca5da-106">Отключает отладку веб-сайта в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca5da-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="ca5da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca5da-107">EXAMPLES</span></span>

### <span data-ttu-id="ca5da-108">--------------Отключить отладку веб-сайта--------------</span><span class="sxs-lookup"><span data-stu-id="ca5da-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="ca5da-109">Отключение отладки веб-сайтов на веб-сайте MyWebsite</span><span class="sxs-lookup"><span data-stu-id="ca5da-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="ca5da-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca5da-110">PARAMETERS</span></span>

### <span data-ttu-id="ca5da-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca5da-111">-Name</span></span>
<span data-ttu-id="ca5da-112">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5da-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="ca5da-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca5da-113">-PassThru</span></span>
<span data-ttu-id="ca5da-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ca5da-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca5da-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ca5da-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca5da-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="ca5da-116">-Profile</span></span>
<span data-ttu-id="ca5da-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ca5da-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca5da-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca5da-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca5da-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ca5da-119">-Slot</span></span>
<span data-ttu-id="ca5da-120">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5da-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="ca5da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5da-121">CommonParameters</span></span>
<span data-ttu-id="ca5da-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca5da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5da-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca5da-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5da-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca5da-124">INPUTS</span></span>

## <span data-ttu-id="ca5da-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca5da-125">OUTPUTS</span></span>

## <span data-ttu-id="ca5da-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca5da-126">NOTES</span></span>

## <span data-ttu-id="ca5da-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca5da-127">RELATED LINKS</span></span>

[<span data-ttu-id="ca5da-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="ca5da-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="ca5da-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca5da-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ca5da-130">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca5da-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="ca5da-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca5da-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="ca5da-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca5da-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


