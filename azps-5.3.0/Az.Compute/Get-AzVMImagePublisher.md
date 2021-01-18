---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519616"
---
# <span data-ttu-id="bcc35-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bcc35-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="bcc35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc35-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc35-103">Получает издателей VMImage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="bcc35-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcc35-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcc35-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcc35-105">DESCRIPTION</span></span>
<span data-ttu-id="bcc35-106">Для **издателей VMImage возвращается cmdlet Get-AzVMImagePublisher.**</span><span class="sxs-lookup"><span data-stu-id="bcc35-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="bcc35-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcc35-107">EXAMPLES</span></span>

### <span data-ttu-id="bcc35-108">Пример 1. Получить издателей VMImage для региона</span><span class="sxs-lookup"><span data-stu-id="bcc35-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="bcc35-109">Эта команда позволяет издателям экземпляров VMImage для центрального региона США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc35-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="bcc35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc35-110">PARAMETERS</span></span>

### <span data-ttu-id="bcc35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc35-111">-DefaultProfile</span></span>
<span data-ttu-id="bcc35-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcc35-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bcc35-113">-Location</span></span>
<span data-ttu-id="bcc35-114">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="bcc35-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc35-115">CommonParameters</span></span>
<span data-ttu-id="bcc35-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc35-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc35-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcc35-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc35-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcc35-118">INPUTS</span></span>

### <span data-ttu-id="bcc35-119">System.String</span><span class="sxs-lookup"><span data-stu-id="bcc35-119">System.String</span></span>

## <span data-ttu-id="bcc35-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcc35-120">OUTPUTS</span></span>

### <span data-ttu-id="bcc35-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bcc35-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="bcc35-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcc35-122">NOTES</span></span>

## <span data-ttu-id="bcc35-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcc35-123">RELATED LINKS</span></span>

[<span data-ttu-id="bcc35-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="bcc35-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="bcc35-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bcc35-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="bcc35-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bcc35-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="bcc35-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="bcc35-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


