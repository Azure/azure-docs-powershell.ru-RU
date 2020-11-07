---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913916"
---
# <span data-ttu-id="fb712-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fb712-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="fb712-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb712-102">SYNOPSIS</span></span>
<span data-ttu-id="fb712-103">Возвращает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb712-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb712-104">SYNTAX</span></span>

### <span data-ttu-id="fb712-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="fb712-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb712-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="fb712-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb712-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb712-107">DESCRIPTION</span></span>
<span data-ttu-id="fb712-108">Командлет **Get-AzureRmVMImage** получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="fb712-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb712-109">EXAMPLES</span></span>

### <span data-ttu-id="fb712-110">Пример 1: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="fb712-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="fb712-111">Эта команда возвращает все версии VMImage, соответствующие указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="fb712-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="fb712-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb712-112">PARAMETERS</span></span>

### <span data-ttu-id="fb712-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb712-113">-DefaultProfile</span></span>
<span data-ttu-id="fb712-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb712-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb712-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="fb712-115">-FilterExpression</span></span>
<span data-ttu-id="fb712-116">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="fb712-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="fb712-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fb712-117">-Location</span></span>
<span data-ttu-id="fb712-118">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="fb712-119">-Предложение</span><span class="sxs-lookup"><span data-stu-id="fb712-119">-Offer</span></span>
<span data-ttu-id="fb712-120">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="fb712-121">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="fb712-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="fb712-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fb712-122">-PublisherName</span></span>
<span data-ttu-id="fb712-123">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="fb712-124">Чтобы получить издатель изображений, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="fb712-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="fb712-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="fb712-125">-Skus</span></span>
<span data-ttu-id="fb712-126">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="fb712-127">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="fb712-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="fb712-128">-Version</span><span class="sxs-lookup"><span data-stu-id="fb712-128">-Version</span></span>
<span data-ttu-id="fb712-129">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="fb712-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="fb712-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb712-130">CommonParameters</span></span>
<span data-ttu-id="fb712-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb712-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb712-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb712-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb712-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb712-133">INPUTS</span></span>

### <span data-ttu-id="fb712-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="fb712-134">None</span></span>
<span data-ttu-id="fb712-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fb712-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb712-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb712-136">OUTPUTS</span></span>

### <span data-ttu-id="fb712-137">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="fb712-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="fb712-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="fb712-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="fb712-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb712-139">NOTES</span></span>

## <span data-ttu-id="fb712-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb712-140">RELATED LINKS</span></span>

[<span data-ttu-id="fb712-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fb712-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fb712-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fb712-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fb712-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fb712-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fb712-144">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fb712-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


