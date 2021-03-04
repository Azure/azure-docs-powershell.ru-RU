---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 7764ee4cd151e3de7cca2af84ed0cf670c52a6a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969288"
---
# <span data-ttu-id="b497a-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="b497a-101">Get-AzGallery</span></span>

## <span data-ttu-id="b497a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b497a-102">SYNOPSIS</span></span>
<span data-ttu-id="b497a-103">Получить или получить коллекций списков.</span><span class="sxs-lookup"><span data-stu-id="b497a-103">Get or list galleries.</span></span>

## <span data-ttu-id="b497a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b497a-104">SYNTAX</span></span>

### <span data-ttu-id="b497a-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b497a-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b497a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b497a-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b497a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b497a-107">DESCRIPTION</span></span>
<span data-ttu-id="b497a-108">Получить или получить коллекций списков.</span><span class="sxs-lookup"><span data-stu-id="b497a-108">Get or list galleries.</span></span>

## <span data-ttu-id="b497a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b497a-109">EXAMPLES</span></span>

### <span data-ttu-id="b497a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b497a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b497a-111">Получить галерею "Галерея1"</span><span class="sxs-lookup"><span data-stu-id="b497a-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="b497a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b497a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b497a-113">Получить все коллекций в rg1.</span><span class="sxs-lookup"><span data-stu-id="b497a-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="b497a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b497a-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b497a-115">Получить все коллекций в подписке.</span><span class="sxs-lookup"><span data-stu-id="b497a-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="b497a-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b497a-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b497a-117">Получите все коллекции в подписке, которые начинаются с "Галерея".</span><span class="sxs-lookup"><span data-stu-id="b497a-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="b497a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b497a-118">PARAMETERS</span></span>

### <span data-ttu-id="b497a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b497a-119">-DefaultProfile</span></span>
<span data-ttu-id="b497a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b497a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b497a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b497a-121">-Name</span></span>
<span data-ttu-id="b497a-122">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="b497a-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b497a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b497a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b497a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b497a-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b497a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b497a-125">-ResourceId</span></span>
<span data-ttu-id="b497a-126">ИД ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="b497a-126">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b497a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b497a-127">CommonParameters</span></span>
<span data-ttu-id="b497a-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b497a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b497a-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b497a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b497a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b497a-130">INPUTS</span></span>

### <span data-ttu-id="b497a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b497a-131">System.String</span></span>

## <span data-ttu-id="b497a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b497a-132">OUTPUTS</span></span>

### <span data-ttu-id="b497a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="b497a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="b497a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b497a-134">NOTES</span></span>

## <span data-ttu-id="b497a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b497a-135">RELATED LINKS</span></span>
