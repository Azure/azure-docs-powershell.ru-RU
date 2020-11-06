---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 881f4ba2d9750c9edbcb988ce3d438e062934a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565459"
---
# <span data-ttu-id="c2752-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c2752-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="c2752-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2752-102">SYNOPSIS</span></span>
<span data-ttu-id="c2752-103">Возвращает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2752-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2752-104">SYNTAX</span></span>

### <span data-ttu-id="c2752-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="c2752-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2752-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="c2752-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2752-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2752-107">DESCRIPTION</span></span>
<span data-ttu-id="c2752-108">Командлет **Get-AzureRmVMImage** получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="c2752-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2752-109">EXAMPLES</span></span>

### <span data-ttu-id="c2752-110">Пример 1: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="c2752-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"
```

<span data-ttu-id="c2752-111">Эта команда возвращает все версии VMImage, соответствующие указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="c2752-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="c2752-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2752-112">PARAMETERS</span></span>

### <span data-ttu-id="c2752-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2752-113">-DefaultProfile</span></span>
<span data-ttu-id="c2752-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2752-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c2752-115">-FilterExpression</span></span>
<span data-ttu-id="c2752-116">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="c2752-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c2752-117">-Location</span></span>
<span data-ttu-id="c2752-118">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-119">-Предложение</span><span class="sxs-lookup"><span data-stu-id="c2752-119">-Offer</span></span>
<span data-ttu-id="c2752-120">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="c2752-121">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="c2752-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c2752-122">-PublisherName</span></span>
<span data-ttu-id="c2752-123">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="c2752-124">Чтобы получить издатель изображений, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c2752-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="c2752-125">-Skus</span></span>
<span data-ttu-id="c2752-126">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="c2752-127">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="c2752-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-128">-Version</span><span class="sxs-lookup"><span data-stu-id="c2752-128">-Version</span></span>
<span data-ttu-id="c2752-129">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="c2752-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2752-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2752-130">CommonParameters</span></span>
<span data-ttu-id="c2752-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2752-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2752-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2752-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2752-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2752-133">INPUTS</span></span>

### <span data-ttu-id="c2752-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2752-134">System.String</span></span>

## <span data-ttu-id="c2752-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2752-135">OUTPUTS</span></span>

### <span data-ttu-id="c2752-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="c2752-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="c2752-137">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="c2752-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="c2752-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2752-138">NOTES</span></span>

## <span data-ttu-id="c2752-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2752-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2752-140">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c2752-140">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="c2752-141">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c2752-141">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c2752-142">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c2752-142">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c2752-143">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c2752-143">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


