---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 983eba222959fb11a50ce94704ebdf39a9bc9fbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013800"
---
# <span data-ttu-id="449e9-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="449e9-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="449e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="449e9-102">SYNOPSIS</span></span>
<span data-ttu-id="449e9-103">Получает издателей VMImage.</span><span class="sxs-lookup"><span data-stu-id="449e9-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="449e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="449e9-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="449e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="449e9-105">DESCRIPTION</span></span>
<span data-ttu-id="449e9-106">Для **издателей VMImage возвращается cmdlet Get-AzVMImagePublisher.**</span><span class="sxs-lookup"><span data-stu-id="449e9-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="449e9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="449e9-107">EXAMPLES</span></span>

### <span data-ttu-id="449e9-108">Пример 1. Получить издателей VMImage для региона</span><span class="sxs-lookup"><span data-stu-id="449e9-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="449e9-109">Эта команда позволяет издателям экземпляров VMImage для центрального региона США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="449e9-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="449e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="449e9-110">PARAMETERS</span></span>

### <span data-ttu-id="449e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449e9-111">-DefaultProfile</span></span>
<span data-ttu-id="449e9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="449e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="449e9-113">-Location</span><span class="sxs-lookup"><span data-stu-id="449e9-113">-Location</span></span>
<span data-ttu-id="449e9-114">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="449e9-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="449e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449e9-115">CommonParameters</span></span>
<span data-ttu-id="449e9-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="449e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449e9-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="449e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449e9-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="449e9-118">INPUTS</span></span>

### <span data-ttu-id="449e9-119">System.String</span><span class="sxs-lookup"><span data-stu-id="449e9-119">System.String</span></span>

## <span data-ttu-id="449e9-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="449e9-120">OUTPUTS</span></span>

### <span data-ttu-id="449e9-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImagePublisher</span><span class="sxs-lookup"><span data-stu-id="449e9-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="449e9-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="449e9-122">NOTES</span></span>

## <span data-ttu-id="449e9-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="449e9-123">RELATED LINKS</span></span>

[<span data-ttu-id="449e9-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="449e9-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="449e9-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="449e9-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="449e9-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="449e9-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="449e9-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="449e9-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


