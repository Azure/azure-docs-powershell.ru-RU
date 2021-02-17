---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233212"
---
# <span data-ttu-id="3edee-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3edee-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="3edee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3edee-102">SYNOPSIS</span></span>
<span data-ttu-id="3edee-103">Создает репликацию контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="3edee-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="3edee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3edee-104">SYNTAX</span></span>

### <span data-ttu-id="3edee-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3edee-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3edee-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3edee-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3edee-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3edee-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3edee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3edee-108">DESCRIPTION</span></span>
<span data-ttu-id="3edee-109">С New-AzContainerRegistryReplication создается репликация контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="3edee-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="3edee-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3edee-110">EXAMPLES</span></span>

### <span data-ttu-id="3edee-111">Пример 1. Создание репликации контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="3edee-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="3edee-112">Создание репликации контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="3edee-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="3edee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3edee-113">PARAMETERS</span></span>

### <span data-ttu-id="3edee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edee-114">-DefaultProfile</span></span>
<span data-ttu-id="3edee-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3edee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3edee-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3edee-116">-Location</span></span>
<span data-ttu-id="3edee-117">Расположение реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="3edee-117">Container Registry Location.</span></span>
<span data-ttu-id="3edee-118">Расположение группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3edee-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3edee-119">-Name</span></span>
<span data-ttu-id="3edee-120">Имя репликации контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="3edee-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="3edee-121">Значение по умолчанию для названия расположения.</span><span class="sxs-lookup"><span data-stu-id="3edee-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="3edee-122">-Registry</span></span>
<span data-ttu-id="3edee-123">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="3edee-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3edee-124">-RegistryName</span></span>
<span data-ttu-id="3edee-125">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="3edee-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3edee-126">-ResourceGroupName</span></span>
<span data-ttu-id="3edee-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3edee-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3edee-128">-ResourceId</span></span>
<span data-ttu-id="3edee-129">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="3edee-129">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="3edee-130">-Tag</span></span>
<span data-ttu-id="3edee-131">Теги контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="3edee-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3edee-132">-Confirm</span></span>
<span data-ttu-id="3edee-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3edee-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edee-134">-WhatIf</span></span>
<span data-ttu-id="3edee-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3edee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3edee-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3edee-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edee-137">CommonParameters</span></span>
<span data-ttu-id="3edee-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3edee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edee-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3edee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edee-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3edee-140">INPUTS</span></span>

### <span data-ttu-id="3edee-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3edee-141">System.String</span></span>

## <span data-ttu-id="3edee-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3edee-142">OUTPUTS</span></span>

### <span data-ttu-id="3edee-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3edee-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="3edee-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3edee-144">NOTES</span></span>

## <span data-ttu-id="3edee-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3edee-145">RELATED LINKS</span></span>

[<span data-ttu-id="3edee-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3edee-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="3edee-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3edee-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)