---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509161"
---
# <span data-ttu-id="584ac-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="584ac-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="584ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="584ac-102">SYNOPSIS</span></span>
<span data-ttu-id="584ac-103">Возвращает типы предложений VMImage.</span><span class="sxs-lookup"><span data-stu-id="584ac-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="584ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="584ac-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="584ac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="584ac-105">DESCRIPTION</span></span>
<span data-ttu-id="584ac-106">Для **получения типов предложений VMImage возвращается cmdlet Get-AzVMImageOffer.**</span><span class="sxs-lookup"><span data-stu-id="584ac-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="584ac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="584ac-107">EXAMPLES</span></span>

### <span data-ttu-id="584ac-108">Пример 1. Типы предложений для издателя</span><span class="sxs-lookup"><span data-stu-id="584ac-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="584ac-109">Эта команда получает типы предложений для указанного издателя в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="584ac-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="584ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="584ac-110">PARAMETERS</span></span>

### <span data-ttu-id="584ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="584ac-111">-DefaultProfile</span></span>
<span data-ttu-id="584ac-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="584ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="584ac-113">-Location</span><span class="sxs-lookup"><span data-stu-id="584ac-113">-Location</span></span>
<span data-ttu-id="584ac-114">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="584ac-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="584ac-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="584ac-115">-PublisherName</span></span>
<span data-ttu-id="584ac-116">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="584ac-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="584ac-117">Чтобы получить издателя, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="584ac-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="584ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584ac-118">CommonParameters</span></span>
<span data-ttu-id="584ac-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584ac-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="584ac-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584ac-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="584ac-121">INPUTS</span></span>

### <span data-ttu-id="584ac-122">System.String</span><span class="sxs-lookup"><span data-stu-id="584ac-122">System.String</span></span>

## <span data-ttu-id="584ac-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="584ac-123">OUTPUTS</span></span>

### <span data-ttu-id="584ac-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImageOffer</span><span class="sxs-lookup"><span data-stu-id="584ac-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="584ac-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="584ac-125">NOTES</span></span>

## <span data-ttu-id="584ac-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="584ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="584ac-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="584ac-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="584ac-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="584ac-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="584ac-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="584ac-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="584ac-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="584ac-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


