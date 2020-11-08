---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078146"
---
# <span data-ttu-id="95f79-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="95f79-101">Get-AzGallery</span></span>

## <span data-ttu-id="95f79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95f79-102">SYNOPSIS</span></span>
<span data-ttu-id="95f79-103">Получение списка коллекций.</span><span class="sxs-lookup"><span data-stu-id="95f79-103">Get or list galleries.</span></span>

## <span data-ttu-id="95f79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95f79-104">SYNTAX</span></span>

### <span data-ttu-id="95f79-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95f79-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95f79-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="95f79-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f79-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f79-107">DESCRIPTION</span></span>
<span data-ttu-id="95f79-108">Получение списка коллекций.</span><span class="sxs-lookup"><span data-stu-id="95f79-108">Get or list galleries.</span></span>

## <span data-ttu-id="95f79-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95f79-109">EXAMPLES</span></span>

### <span data-ttu-id="95f79-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95f79-110">Example 1</span></span>
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

<span data-ttu-id="95f79-111">Получение коллекции "gallery1"</span><span class="sxs-lookup"><span data-stu-id="95f79-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="95f79-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="95f79-112">Example 2</span></span>
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

<span data-ttu-id="95f79-113">Получение всех коллекций в Rg1.</span><span class="sxs-lookup"><span data-stu-id="95f79-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="95f79-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="95f79-114">Example 3</span></span>
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

<span data-ttu-id="95f79-115">Получение всех коллекций в подписке.</span><span class="sxs-lookup"><span data-stu-id="95f79-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="95f79-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="95f79-116">Example 4</span></span>
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

<span data-ttu-id="95f79-117">Получение всех коллекций подписок, которые начинаются со слова "Коллекция".</span><span class="sxs-lookup"><span data-stu-id="95f79-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="95f79-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95f79-118">PARAMETERS</span></span>

### <span data-ttu-id="95f79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f79-119">-DefaultProfile</span></span>
<span data-ttu-id="95f79-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95f79-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95f79-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95f79-121">-Name</span></span>
<span data-ttu-id="95f79-122">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="95f79-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="95f79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f79-123">-ResourceGroupName</span></span>
<span data-ttu-id="95f79-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95f79-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="95f79-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95f79-125">-ResourceId</span></span>
<span data-ttu-id="95f79-126">Идентификатор ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="95f79-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="95f79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f79-127">CommonParameters</span></span>
<span data-ttu-id="95f79-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95f79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f79-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95f79-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f79-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95f79-130">INPUTS</span></span>

### <span data-ttu-id="95f79-131">System. String</span><span class="sxs-lookup"><span data-stu-id="95f79-131">System.String</span></span>

## <span data-ttu-id="95f79-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f79-132">OUTPUTS</span></span>

### <span data-ttu-id="95f79-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="95f79-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="95f79-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="95f79-134">NOTES</span></span>

## <span data-ttu-id="95f79-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95f79-135">RELATED LINKS</span></span>
