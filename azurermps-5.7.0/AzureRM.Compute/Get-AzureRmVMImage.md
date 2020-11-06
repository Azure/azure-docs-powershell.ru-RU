---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559195"
---
# <span data-ttu-id="9edc7-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9edc7-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="9edc7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9edc7-102">SYNOPSIS</span></span>
<span data-ttu-id="9edc7-103">Возвращает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9edc7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9edc7-104">SYNTAX</span></span>

### <span data-ttu-id="9edc7-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9edc7-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="9edc7-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9edc7-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="9edc7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9edc7-107">DESCRIPTION</span></span>
<span data-ttu-id="9edc7-108">Командлет **Get-AzureRmVMImage** получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9edc7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9edc7-109">EXAMPLES</span></span>

### <span data-ttu-id="9edc7-110">Пример 1: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="9edc7-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="9edc7-111">Эта команда возвращает все версии VMImage, соответствующие указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="9edc7-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="9edc7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9edc7-112">PARAMETERS</span></span>

### <span data-ttu-id="9edc7-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9edc7-113">-FilterExpression</span></span>
<span data-ttu-id="9edc7-114">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="9edc7-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9edc7-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9edc7-115">-Location</span></span>
<span data-ttu-id="9edc7-116">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-116">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9edc7-117">-Предложение</span><span class="sxs-lookup"><span data-stu-id="9edc7-117">-Offer</span></span>
<span data-ttu-id="9edc7-118">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9edc7-119">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="9edc7-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9edc7-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9edc7-120">-PublisherName</span></span>
<span data-ttu-id="9edc7-121">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9edc7-122">Чтобы получить издатель изображений, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9edc7-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9edc7-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="9edc7-123">-Skus</span></span>
<span data-ttu-id="9edc7-124">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9edc7-125">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9edc7-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9edc7-126">-Version</span><span class="sxs-lookup"><span data-stu-id="9edc7-126">-Version</span></span>
<span data-ttu-id="9edc7-127">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="9edc7-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9edc7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9edc7-128">CommonParameters</span></span>
<span data-ttu-id="9edc7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9edc7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9edc7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9edc7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9edc7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9edc7-131">INPUTS</span></span>

### <span data-ttu-id="9edc7-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="9edc7-132">None</span></span>
<span data-ttu-id="9edc7-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9edc7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9edc7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9edc7-134">OUTPUTS</span></span>

## <span data-ttu-id="9edc7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9edc7-135">NOTES</span></span>

## <span data-ttu-id="9edc7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9edc7-136">RELATED LINKS</span></span>

[<span data-ttu-id="9edc7-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9edc7-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="9edc7-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9edc7-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="9edc7-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9edc7-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9edc7-140">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9edc7-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


