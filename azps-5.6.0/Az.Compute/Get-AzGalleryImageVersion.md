---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 6122bd17828b07e47f41c3f2d087f88d468ca6be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969256"
---
# <span data-ttu-id="55aaf-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="55aaf-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="55aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="55aaf-103">Получить или получить версии изображений из коллекции списков.</span><span class="sxs-lookup"><span data-stu-id="55aaf-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="55aaf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55aaf-104">SYNTAX</span></span>

### <span data-ttu-id="55aaf-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55aaf-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55aaf-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="55aaf-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55aaf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55aaf-107">DESCRIPTION</span></span>
<span data-ttu-id="55aaf-108">Получить или получить версии изображений из коллекции списков.</span><span class="sxs-lookup"><span data-stu-id="55aaf-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="55aaf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55aaf-109">EXAMPLES</span></span>

### <span data-ttu-id="55aaf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55aaf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="55aaf-111">Получить версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="55aaf-111">Get the gallery image version.</span></span>

### <span data-ttu-id="55aaf-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="55aaf-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="55aaf-113">Получите версии изображений из коллекции, которые начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="55aaf-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="55aaf-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="55aaf-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="55aaf-115">Получить все версии изображений коллекции.</span><span class="sxs-lookup"><span data-stu-id="55aaf-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="55aaf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55aaf-116">PARAMETERS</span></span>

### <span data-ttu-id="55aaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55aaf-117">-DefaultProfile</span></span>
<span data-ttu-id="55aaf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55aaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55aaf-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="55aaf-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="55aaf-120">Показать состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="55aaf-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aaf-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="55aaf-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="55aaf-122">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="55aaf-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aaf-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="55aaf-123">-GalleryName</span></span>
<span data-ttu-id="55aaf-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="55aaf-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aaf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="55aaf-125">-Name</span></span>
<span data-ttu-id="55aaf-126">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="55aaf-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="55aaf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55aaf-127">-ResourceGroupName</span></span>
<span data-ttu-id="55aaf-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55aaf-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aaf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55aaf-129">-ResourceId</span></span>
<span data-ttu-id="55aaf-130">ИД ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="55aaf-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="55aaf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55aaf-131">CommonParameters</span></span>
<span data-ttu-id="55aaf-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55aaf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55aaf-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55aaf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55aaf-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55aaf-134">INPUTS</span></span>

### <span data-ttu-id="55aaf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="55aaf-135">System.String</span></span>

### <span data-ttu-id="55aaf-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55aaf-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55aaf-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55aaf-137">OUTPUTS</span></span>

### <span data-ttu-id="55aaf-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="55aaf-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="55aaf-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55aaf-139">NOTES</span></span>

## <span data-ttu-id="55aaf-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55aaf-140">RELATED LINKS</span></span>
