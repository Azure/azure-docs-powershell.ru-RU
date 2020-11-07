---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914621"
---
# <span data-ttu-id="4c189-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4c189-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="4c189-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c189-102">SYNOPSIS</span></span>
<span data-ttu-id="4c189-103">Возвращает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="4c189-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c189-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c189-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c189-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c189-105">DESCRIPTION</span></span>
<span data-ttu-id="4c189-106">Командлет **Get-AzureRmVMImageSku** получает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="4c189-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="4c189-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c189-107">EXAMPLES</span></span>

### <span data-ttu-id="4c189-108">Пример 1: получение конфигураций VMImage</span><span class="sxs-lookup"><span data-stu-id="4c189-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="4c189-109">Эта команда возвращает SKU для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="4c189-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="4c189-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c189-110">PARAMETERS</span></span>

### <span data-ttu-id="4c189-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c189-111">-DefaultProfile</span></span>
<span data-ttu-id="4c189-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c189-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c189-113">-Location</span><span class="sxs-lookup"><span data-stu-id="4c189-113">-Location</span></span>
<span data-ttu-id="4c189-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="4c189-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4c189-115">-Предложение</span><span class="sxs-lookup"><span data-stu-id="4c189-115">-Offer</span></span>
<span data-ttu-id="4c189-116">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="4c189-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="4c189-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4c189-117">-PublisherName</span></span>
<span data-ttu-id="4c189-118">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="4c189-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="4c189-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c189-119">CommonParameters</span></span>
<span data-ttu-id="4c189-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c189-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c189-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c189-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c189-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c189-122">INPUTS</span></span>

### <span data-ttu-id="4c189-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c189-123">None</span></span>
<span data-ttu-id="4c189-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4c189-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c189-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c189-125">OUTPUTS</span></span>

### <span data-ttu-id="4c189-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="4c189-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="4c189-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c189-127">NOTES</span></span>

## <span data-ttu-id="4c189-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c189-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c189-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4c189-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4c189-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4c189-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4c189-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4c189-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4c189-132">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4c189-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


