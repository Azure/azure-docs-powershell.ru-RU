---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403108"
---
# <span data-ttu-id="a44ec-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a44ec-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="a44ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a44ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a44ec-103">Получает skus VMImage.</span><span class="sxs-lookup"><span data-stu-id="a44ec-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="a44ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a44ec-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a44ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a44ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a44ec-106">Для **получения skus -VMImage возвращается cmdlet Get-AzVMImageSku.**</span><span class="sxs-lookup"><span data-stu-id="a44ec-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="a44ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a44ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a44ec-108">Пример 1. Получить skUs VMImage</span><span class="sxs-lookup"><span data-stu-id="a44ec-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="a44ec-109">Эта команда получает skus для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="a44ec-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="a44ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a44ec-110">PARAMETERS</span></span>

### <span data-ttu-id="a44ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44ec-111">-DefaultProfile</span></span>
<span data-ttu-id="a44ec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a44ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a44ec-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a44ec-113">-Location</span></span>
<span data-ttu-id="a44ec-114">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="a44ec-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="a44ec-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="a44ec-115">-Offer</span></span>
<span data-ttu-id="a44ec-116">Тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="a44ec-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="a44ec-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a44ec-117">-PublisherName</span></span>
<span data-ttu-id="a44ec-118">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="a44ec-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="a44ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44ec-119">CommonParameters</span></span>
<span data-ttu-id="a44ec-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44ec-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a44ec-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44ec-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a44ec-122">INPUTS</span></span>

### <span data-ttu-id="a44ec-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a44ec-123">System.String</span></span>

## <span data-ttu-id="a44ec-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a44ec-124">OUTPUTS</span></span>

### <span data-ttu-id="a44ec-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImageSku</span><span class="sxs-lookup"><span data-stu-id="a44ec-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="a44ec-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a44ec-126">NOTES</span></span>

## <span data-ttu-id="a44ec-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a44ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="a44ec-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a44ec-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a44ec-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a44ec-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a44ec-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a44ec-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a44ec-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a44ec-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


