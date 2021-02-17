---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233188"
---
# <span data-ttu-id="0ca14-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ca14-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="0ca14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca14-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca14-103">Удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="0ca14-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="0ca14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ca14-104">SYNTAX</span></span>

### <span data-ttu-id="0ca14-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ca14-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca14-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca14-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca14-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca14-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ca14-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ca14-108">DESCRIPTION</span></span>
<span data-ttu-id="0ca14-109">Этот Remove-AzContainerRegistryReplication удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="0ca14-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="0ca14-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ca14-110">EXAMPLES</span></span>

### <span data-ttu-id="0ca14-111">Пример 1. Удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="0ca14-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="0ca14-112">Удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="0ca14-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="0ca14-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ca14-113">PARAMETERS</span></span>

### <span data-ttu-id="0ca14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca14-114">-DefaultProfile</span></span>
<span data-ttu-id="0ca14-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca14-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca14-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0ca14-116">-Name</span></span>
<span data-ttu-id="0ca14-117">Имя репликации контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="0ca14-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="0ca14-118">Значение по умолчанию для имени расположения.</span><span class="sxs-lookup"><span data-stu-id="0ca14-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca14-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ca14-119">-PassThru</span></span>
<span data-ttu-id="0ca14-120">Указывает на то, что этот cmdlet возвращает истина, если удаление было успешно.</span><span class="sxs-lookup"><span data-stu-id="0ca14-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca14-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0ca14-121">-RegistryName</span></span>
<span data-ttu-id="0ca14-122">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="0ca14-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca14-123">-Репликация</span><span class="sxs-lookup"><span data-stu-id="0ca14-123">-Replication</span></span>
<span data-ttu-id="0ca14-124">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="0ca14-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca14-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca14-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ca14-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ca14-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca14-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca14-127">-ResourceId</span></span>
<span data-ttu-id="0ca14-128">ИД ресурса репликации контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="0ca14-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="0ca14-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ca14-129">-Confirm</span></span>
<span data-ttu-id="0ca14-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0ca14-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca14-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca14-131">-WhatIf</span></span>
<span data-ttu-id="0ca14-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ca14-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ca14-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ca14-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca14-134">CommonParameters</span></span>
<span data-ttu-id="0ca14-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca14-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ca14-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca14-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ca14-137">INPUTS</span></span>

### <span data-ttu-id="0ca14-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ca14-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="0ca14-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0ca14-139">System.String</span></span>

## <span data-ttu-id="0ca14-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ca14-140">OUTPUTS</span></span>

### <span data-ttu-id="0ca14-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ca14-141">System.Boolean</span></span>

## <span data-ttu-id="0ca14-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ca14-142">NOTES</span></span>

## <span data-ttu-id="0ca14-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ca14-143">RELATED LINKS</span></span>

[<span data-ttu-id="0ca14-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ca14-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="0ca14-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ca14-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

