---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 4eea328b83b4d4ad70ba755e4875168b6b35ecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013747"
---
# <span data-ttu-id="4e428-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4e428-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="4e428-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e428-102">SYNOPSIS</span></span>
<span data-ttu-id="4e428-103">Получает skus VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e428-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="4e428-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e428-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e428-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e428-105">DESCRIPTION</span></span>
<span data-ttu-id="4e428-106">Для **получения skus -VMImage возвращается cmdlet Get-AzVMImageSku.**</span><span class="sxs-lookup"><span data-stu-id="4e428-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="4e428-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e428-107">EXAMPLES</span></span>

### <span data-ttu-id="4e428-108">Пример 1. Получить skUs VMImage</span><span class="sxs-lookup"><span data-stu-id="4e428-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="4e428-109">Эта команда получает skus для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="4e428-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="4e428-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e428-110">PARAMETERS</span></span>

### <span data-ttu-id="4e428-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e428-111">-DefaultProfile</span></span>
<span data-ttu-id="4e428-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e428-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e428-113">-Location</span><span class="sxs-lookup"><span data-stu-id="4e428-113">-Location</span></span>
<span data-ttu-id="4e428-114">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e428-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4e428-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="4e428-115">-Offer</span></span>
<span data-ttu-id="4e428-116">Тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e428-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="4e428-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4e428-117">-PublisherName</span></span>
<span data-ttu-id="4e428-118">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e428-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="4e428-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e428-119">CommonParameters</span></span>
<span data-ttu-id="4e428-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e428-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e428-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e428-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e428-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e428-122">INPUTS</span></span>

### <span data-ttu-id="4e428-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4e428-123">System.String</span></span>

## <span data-ttu-id="4e428-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e428-124">OUTPUTS</span></span>

### <span data-ttu-id="4e428-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImageSku</span><span class="sxs-lookup"><span data-stu-id="4e428-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="4e428-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e428-126">NOTES</span></span>

## <span data-ttu-id="4e428-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e428-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e428-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4e428-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="4e428-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4e428-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="4e428-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4e428-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="4e428-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4e428-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


