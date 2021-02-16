---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233356"
---
# <span data-ttu-id="88283-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="88283-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="88283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88283-102">SYNOPSIS</span></span>
<span data-ttu-id="88283-103">Получает издателей VMImage.</span><span class="sxs-lookup"><span data-stu-id="88283-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="88283-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88283-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88283-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88283-105">DESCRIPTION</span></span>
<span data-ttu-id="88283-106">Для **издателей VMImage возвращается cmdlet Get-AzVMImagePublisher.**</span><span class="sxs-lookup"><span data-stu-id="88283-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="88283-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88283-107">EXAMPLES</span></span>

### <span data-ttu-id="88283-108">Пример 1. Получить издателей VMImage для региона</span><span class="sxs-lookup"><span data-stu-id="88283-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="88283-109">Эта команда позволяет издателям экземпляров VMImage для центрального региона США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="88283-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="88283-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88283-110">PARAMETERS</span></span>

### <span data-ttu-id="88283-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88283-111">-DefaultProfile</span></span>
<span data-ttu-id="88283-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88283-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88283-113">-Location</span><span class="sxs-lookup"><span data-stu-id="88283-113">-Location</span></span>
<span data-ttu-id="88283-114">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="88283-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="88283-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88283-115">CommonParameters</span></span>
<span data-ttu-id="88283-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88283-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88283-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88283-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88283-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88283-118">INPUTS</span></span>

### <span data-ttu-id="88283-119">System.String</span><span class="sxs-lookup"><span data-stu-id="88283-119">System.String</span></span>

## <span data-ttu-id="88283-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88283-120">OUTPUTS</span></span>

### <span data-ttu-id="88283-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImagePublisher</span><span class="sxs-lookup"><span data-stu-id="88283-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="88283-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88283-122">NOTES</span></span>

## <span data-ttu-id="88283-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88283-123">RELATED LINKS</span></span>

[<span data-ttu-id="88283-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="88283-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="88283-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="88283-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="88283-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="88283-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="88283-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="88283-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


