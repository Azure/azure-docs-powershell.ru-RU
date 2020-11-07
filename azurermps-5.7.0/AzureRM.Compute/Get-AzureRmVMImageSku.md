---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734480"
---
# <span data-ttu-id="d4022-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d4022-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="d4022-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4022-102">SYNOPSIS</span></span>
<span data-ttu-id="d4022-103">Возвращает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="d4022-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4022-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4022-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="d4022-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4022-105">DESCRIPTION</span></span>
<span data-ttu-id="d4022-106">Командлет **Get-AzureRmVMImageSku** получает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="d4022-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="d4022-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4022-107">EXAMPLES</span></span>

### <span data-ttu-id="d4022-108">Пример 1: получение конфигураций VMImage</span><span class="sxs-lookup"><span data-stu-id="d4022-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="d4022-109">Эта команда возвращает SKU для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="d4022-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="d4022-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4022-110">PARAMETERS</span></span>

### <span data-ttu-id="d4022-111">-Location</span><span class="sxs-lookup"><span data-stu-id="d4022-111">-Location</span></span>
<span data-ttu-id="d4022-112">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="d4022-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="d4022-113">-Предложение</span><span class="sxs-lookup"><span data-stu-id="d4022-113">-Offer</span></span>
<span data-ttu-id="d4022-114">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="d4022-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="d4022-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d4022-115">-PublisherName</span></span>
<span data-ttu-id="d4022-116">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="d4022-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="d4022-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4022-117">CommonParameters</span></span>
<span data-ttu-id="d4022-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4022-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4022-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4022-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4022-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4022-120">INPUTS</span></span>

### <span data-ttu-id="d4022-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="d4022-121">None</span></span>
<span data-ttu-id="d4022-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d4022-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4022-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4022-123">OUTPUTS</span></span>

## <span data-ttu-id="d4022-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4022-124">NOTES</span></span>

## <span data-ttu-id="d4022-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4022-125">RELATED LINKS</span></span>

[<span data-ttu-id="d4022-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d4022-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="d4022-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d4022-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="d4022-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d4022-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="d4022-129">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d4022-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


