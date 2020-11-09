---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318128"
---
# <span data-ttu-id="f8486-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f8486-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f8486-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8486-102">SYNOPSIS</span></span>
<span data-ttu-id="f8486-103">Получение и перечисление версий изображений коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="f8486-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8486-104">SYNTAX</span></span>

### <span data-ttu-id="f8486-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8486-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8486-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f8486-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8486-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8486-107">DESCRIPTION</span></span>
<span data-ttu-id="f8486-108">Получение и перечисление версий изображений коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="f8486-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8486-109">EXAMPLES</span></span>

### <span data-ttu-id="f8486-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8486-110">Example 1</span></span>
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

<span data-ttu-id="f8486-111">Получить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-111">Get the gallery image version.</span></span>

### <span data-ttu-id="f8486-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f8486-112">Example 2</span></span>
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

<span data-ttu-id="f8486-113">Получение версий изображений коллекции, начинающихся с "1".</span><span class="sxs-lookup"><span data-stu-id="f8486-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="f8486-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f8486-114">Example 3</span></span>
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

<span data-ttu-id="f8486-115">Получить все версии изображений коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="f8486-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8486-116">PARAMETERS</span></span>

### <span data-ttu-id="f8486-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8486-117">-DefaultProfile</span></span>
<span data-ttu-id="f8486-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8486-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8486-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="f8486-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="f8486-120">Показать состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="f8486-120">Show replication status.</span></span>

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

### <span data-ttu-id="f8486-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f8486-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f8486-122">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="f8486-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f8486-123">-GalleryName</span></span>
<span data-ttu-id="f8486-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="f8486-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8486-125">-Name</span></span>
<span data-ttu-id="f8486-126">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8486-126">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="f8486-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8486-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8486-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8486-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8486-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8486-129">-ResourceId</span></span>
<span data-ttu-id="f8486-130">Идентификатор ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="f8486-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="f8486-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8486-131">CommonParameters</span></span>
<span data-ttu-id="f8486-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8486-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8486-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8486-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8486-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8486-134">INPUTS</span></span>

### <span data-ttu-id="f8486-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f8486-135">System.String</span></span>

### <span data-ttu-id="f8486-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8486-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8486-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8486-137">OUTPUTS</span></span>

### <span data-ttu-id="f8486-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f8486-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f8486-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8486-139">NOTES</span></span>

## <span data-ttu-id="f8486-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8486-140">RELATED LINKS</span></span>
