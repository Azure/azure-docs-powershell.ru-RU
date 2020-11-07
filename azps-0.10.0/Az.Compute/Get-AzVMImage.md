---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911522"
---
# <span data-ttu-id="37424-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="37424-101">Get-AzVMImage</span></span>

## <span data-ttu-id="37424-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37424-102">SYNOPSIS</span></span>
<span data-ttu-id="37424-103">Возвращает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="37424-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37424-104">SYNTAX</span></span>

### <span data-ttu-id="37424-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="37424-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37424-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="37424-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37424-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37424-107">DESCRIPTION</span></span>
<span data-ttu-id="37424-108">Командлет **Get-AzVMImage** получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="37424-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37424-109">EXAMPLES</span></span>

### <span data-ttu-id="37424-110">Пример 1: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="37424-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="37424-111">Эта команда возвращает все версии VMImage, соответствующие указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="37424-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="37424-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37424-112">PARAMETERS</span></span>

### <span data-ttu-id="37424-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37424-113">-DefaultProfile</span></span>
<span data-ttu-id="37424-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37424-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37424-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="37424-115">-FilterExpression</span></span>
<span data-ttu-id="37424-116">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="37424-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="37424-117">-Location</span><span class="sxs-lookup"><span data-stu-id="37424-117">-Location</span></span>
<span data-ttu-id="37424-118">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="37424-119">-Предложение</span><span class="sxs-lookup"><span data-stu-id="37424-119">-Offer</span></span>
<span data-ttu-id="37424-120">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="37424-121">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="37424-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="37424-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="37424-122">-PublisherName</span></span>
<span data-ttu-id="37424-123">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="37424-124">Чтобы получить издатель изображений, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="37424-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="37424-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="37424-125">-Skus</span></span>
<span data-ttu-id="37424-126">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="37424-127">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="37424-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="37424-128">-Version</span><span class="sxs-lookup"><span data-stu-id="37424-128">-Version</span></span>
<span data-ttu-id="37424-129">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="37424-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="37424-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37424-130">CommonParameters</span></span>
<span data-ttu-id="37424-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37424-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37424-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37424-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37424-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37424-133">INPUTS</span></span>

### <span data-ttu-id="37424-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="37424-134">None</span></span>
<span data-ttu-id="37424-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="37424-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37424-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37424-136">OUTPUTS</span></span>

### <span data-ttu-id="37424-137">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="37424-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="37424-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="37424-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="37424-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="37424-139">NOTES</span></span>

## <span data-ttu-id="37424-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37424-140">RELATED LINKS</span></span>

[<span data-ttu-id="37424-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="37424-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="37424-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="37424-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="37424-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="37424-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="37424-144">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="37424-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


