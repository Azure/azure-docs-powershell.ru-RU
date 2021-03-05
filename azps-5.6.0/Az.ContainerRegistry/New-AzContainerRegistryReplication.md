---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995714"
---
# <span data-ttu-id="85eba-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85eba-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="85eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85eba-102">SYNOPSIS</span></span>
<span data-ttu-id="85eba-103">Создает репликацию контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="85eba-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="85eba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85eba-104">SYNTAX</span></span>

### <span data-ttu-id="85eba-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85eba-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85eba-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85eba-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85eba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85eba-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85eba-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85eba-108">DESCRIPTION</span></span>
<span data-ttu-id="85eba-109">С New-AzContainerRegistryReplication создается репликация контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="85eba-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="85eba-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85eba-110">EXAMPLES</span></span>

### <span data-ttu-id="85eba-111">Пример 1. Создание репликации контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="85eba-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="85eba-112">Создание репликации контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="85eba-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="85eba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85eba-113">PARAMETERS</span></span>

### <span data-ttu-id="85eba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85eba-114">-DefaultProfile</span></span>
<span data-ttu-id="85eba-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85eba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85eba-116">-Location</span><span class="sxs-lookup"><span data-stu-id="85eba-116">-Location</span></span>
<span data-ttu-id="85eba-117">Расположение реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="85eba-117">Container Registry Location.</span></span>
<span data-ttu-id="85eba-118">Расположение группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85eba-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="85eba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="85eba-119">-Name</span></span>
<span data-ttu-id="85eba-120">Имя репликации контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="85eba-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="85eba-121">Значение по умолчанию для названия расположения.</span><span class="sxs-lookup"><span data-stu-id="85eba-121">Default to the location name.</span></span>

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

### <span data-ttu-id="85eba-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="85eba-122">-Registry</span></span>
<span data-ttu-id="85eba-123">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="85eba-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="85eba-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="85eba-124">-RegistryName</span></span>
<span data-ttu-id="85eba-125">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="85eba-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="85eba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85eba-126">-ResourceGroupName</span></span>
<span data-ttu-id="85eba-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85eba-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="85eba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85eba-128">-ResourceId</span></span>
<span data-ttu-id="85eba-129">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="85eba-129">The container registry resource id</span></span>

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

### <span data-ttu-id="85eba-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="85eba-130">-Tag</span></span>
<span data-ttu-id="85eba-131">Теги контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="85eba-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="85eba-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85eba-132">-Confirm</span></span>
<span data-ttu-id="85eba-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85eba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85eba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85eba-134">-WhatIf</span></span>
<span data-ttu-id="85eba-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85eba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85eba-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="85eba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85eba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85eba-137">CommonParameters</span></span>
<span data-ttu-id="85eba-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85eba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85eba-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85eba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85eba-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85eba-140">INPUTS</span></span>

### <span data-ttu-id="85eba-141">System.String</span><span class="sxs-lookup"><span data-stu-id="85eba-141">System.String</span></span>

## <span data-ttu-id="85eba-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85eba-142">OUTPUTS</span></span>

### <span data-ttu-id="85eba-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85eba-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="85eba-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85eba-144">NOTES</span></span>

## <span data-ttu-id="85eba-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85eba-145">RELATED LINKS</span></span>

[<span data-ttu-id="85eba-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85eba-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="85eba-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85eba-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)