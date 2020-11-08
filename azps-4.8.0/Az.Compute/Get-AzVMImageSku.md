---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235665"
---
# <span data-ttu-id="8d699-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8d699-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="8d699-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d699-102">SYNOPSIS</span></span>
<span data-ttu-id="8d699-103">Возвращает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="8d699-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="8d699-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d699-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d699-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d699-105">DESCRIPTION</span></span>
<span data-ttu-id="8d699-106">Командлет **Get-AzVMImageSku** получает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="8d699-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="8d699-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d699-107">EXAMPLES</span></span>

### <span data-ttu-id="8d699-108">Пример 1: получение конфигураций VMImage</span><span class="sxs-lookup"><span data-stu-id="8d699-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="8d699-109">Эта команда возвращает SKU для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="8d699-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="8d699-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d699-110">PARAMETERS</span></span>

### <span data-ttu-id="8d699-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d699-111">-DefaultProfile</span></span>
<span data-ttu-id="8d699-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d699-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d699-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8d699-113">-Location</span></span>
<span data-ttu-id="8d699-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d699-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="8d699-115">-Предложение</span><span class="sxs-lookup"><span data-stu-id="8d699-115">-Offer</span></span>
<span data-ttu-id="8d699-116">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d699-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="8d699-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="8d699-117">-PublisherName</span></span>
<span data-ttu-id="8d699-118">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d699-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="8d699-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d699-119">CommonParameters</span></span>
<span data-ttu-id="8d699-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d699-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d699-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d699-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d699-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d699-122">INPUTS</span></span>

### <span data-ttu-id="8d699-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8d699-123">System.String</span></span>

## <span data-ttu-id="8d699-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d699-124">OUTPUTS</span></span>

### <span data-ttu-id="8d699-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="8d699-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="8d699-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d699-126">NOTES</span></span>

## <span data-ttu-id="8d699-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d699-127">RELATED LINKS</span></span>

[<span data-ttu-id="8d699-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8d699-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="8d699-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8d699-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="8d699-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8d699-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8d699-131">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8d699-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


