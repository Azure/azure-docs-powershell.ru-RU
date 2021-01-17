---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392980"
---
# <span data-ttu-id="e7764-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="e7764-101">Get-AzGallery</span></span>

## <span data-ttu-id="e7764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7764-102">SYNOPSIS</span></span>
<span data-ttu-id="e7764-103">Получить или получить коллекций списков.</span><span class="sxs-lookup"><span data-stu-id="e7764-103">Get or list galleries.</span></span>

## <span data-ttu-id="e7764-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7764-104">SYNTAX</span></span>

### <span data-ttu-id="e7764-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7764-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7764-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e7764-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7764-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7764-107">DESCRIPTION</span></span>
<span data-ttu-id="e7764-108">Получить или получить коллекций списков.</span><span class="sxs-lookup"><span data-stu-id="e7764-108">Get or list galleries.</span></span>

## <span data-ttu-id="e7764-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7764-109">EXAMPLES</span></span>

### <span data-ttu-id="e7764-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7764-110">Example 1</span></span>
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

<span data-ttu-id="e7764-111">Получить галерею "Галерея1"</span><span class="sxs-lookup"><span data-stu-id="e7764-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="e7764-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e7764-112">Example 2</span></span>
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

<span data-ttu-id="e7764-113">Получить все коллекций в rg1.</span><span class="sxs-lookup"><span data-stu-id="e7764-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="e7764-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e7764-114">Example 3</span></span>
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

<span data-ttu-id="e7764-115">Получить все коллекций в подписке.</span><span class="sxs-lookup"><span data-stu-id="e7764-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="e7764-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e7764-116">Example 4</span></span>
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

<span data-ttu-id="e7764-117">Получите все коллекции в подписке, которые начинаются с "Галерея".</span><span class="sxs-lookup"><span data-stu-id="e7764-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="e7764-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7764-118">PARAMETERS</span></span>

### <span data-ttu-id="e7764-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7764-119">-DefaultProfile</span></span>
<span data-ttu-id="e7764-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7764-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7764-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e7764-121">-Name</span></span>
<span data-ttu-id="e7764-122">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="e7764-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="e7764-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7764-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7764-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7764-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7764-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7764-125">-ResourceId</span></span>
<span data-ttu-id="e7764-126">ИД ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="e7764-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="e7764-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7764-127">CommonParameters</span></span>
<span data-ttu-id="e7764-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7764-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7764-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7764-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7764-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7764-130">INPUTS</span></span>

### <span data-ttu-id="e7764-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e7764-131">System.String</span></span>

## <span data-ttu-id="e7764-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7764-132">OUTPUTS</span></span>

### <span data-ttu-id="e7764-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="e7764-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="e7764-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7764-134">NOTES</span></span>

## <span data-ttu-id="e7764-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7764-135">RELATED LINKS</span></span>
