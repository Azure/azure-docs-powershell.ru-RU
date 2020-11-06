---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5131a9ea24ea14114c9a4d5f5600bbe190499f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565456"
---
# <span data-ttu-id="32473-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="32473-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="32473-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32473-102">SYNOPSIS</span></span>
<span data-ttu-id="32473-103">Возвращает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="32473-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32473-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32473-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32473-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32473-105">DESCRIPTION</span></span>
<span data-ttu-id="32473-106">Командлет **Get-AzureRmVMImageSku** получает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="32473-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="32473-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32473-107">EXAMPLES</span></span>

### <span data-ttu-id="32473-108">Пример 1: получение конфигураций VMImage</span><span class="sxs-lookup"><span data-stu-id="32473-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="32473-109">Эта команда возвращает SKU для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="32473-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="32473-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32473-110">PARAMETERS</span></span>

### <span data-ttu-id="32473-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32473-111">-DefaultProfile</span></span>
<span data-ttu-id="32473-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32473-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32473-113">-Location</span><span class="sxs-lookup"><span data-stu-id="32473-113">-Location</span></span>
<span data-ttu-id="32473-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="32473-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="32473-115">-Предложение</span><span class="sxs-lookup"><span data-stu-id="32473-115">-Offer</span></span>
<span data-ttu-id="32473-116">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="32473-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="32473-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="32473-117">-PublisherName</span></span>
<span data-ttu-id="32473-118">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="32473-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="32473-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32473-119">CommonParameters</span></span>
<span data-ttu-id="32473-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32473-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32473-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32473-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32473-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32473-122">INPUTS</span></span>

### <span data-ttu-id="32473-123">System. String</span><span class="sxs-lookup"><span data-stu-id="32473-123">System.String</span></span>

## <span data-ttu-id="32473-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32473-124">OUTPUTS</span></span>

### <span data-ttu-id="32473-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="32473-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="32473-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="32473-126">NOTES</span></span>

## <span data-ttu-id="32473-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32473-127">RELATED LINKS</span></span>

[<span data-ttu-id="32473-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="32473-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="32473-129">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="32473-129">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="32473-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="32473-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="32473-131">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="32473-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


