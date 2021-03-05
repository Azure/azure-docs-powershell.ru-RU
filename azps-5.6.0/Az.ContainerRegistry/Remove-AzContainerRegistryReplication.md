---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 3fff7a0952f4ace41f76237a8fbf226e9bb58128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015379"
---
# <span data-ttu-id="8d07d-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8d07d-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="8d07d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d07d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d07d-103">Удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8d07d-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="8d07d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d07d-104">SYNTAX</span></span>

### <span data-ttu-id="8d07d-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d07d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d07d-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d07d-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d07d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d07d-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d07d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d07d-108">DESCRIPTION</span></span>
<span data-ttu-id="8d07d-109">Этот Remove-AzContainerRegistryReplication удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8d07d-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="8d07d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d07d-110">EXAMPLES</span></span>

### <span data-ttu-id="8d07d-111">Пример 1. Удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8d07d-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="8d07d-112">Удаляет репликацию контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8d07d-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="8d07d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d07d-113">PARAMETERS</span></span>

### <span data-ttu-id="8d07d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d07d-114">-DefaultProfile</span></span>
<span data-ttu-id="8d07d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d07d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d07d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8d07d-116">-Name</span></span>
<span data-ttu-id="8d07d-117">Имя репликации контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="8d07d-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="8d07d-118">Значение по умолчанию для названия расположения.</span><span class="sxs-lookup"><span data-stu-id="8d07d-118">Default to the location name.</span></span>

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

### <span data-ttu-id="8d07d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d07d-119">-PassThru</span></span>
<span data-ttu-id="8d07d-120">Указывает на то, что этот cmdlet возвращает истина, если удаление было успешно.</span><span class="sxs-lookup"><span data-stu-id="8d07d-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8d07d-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8d07d-121">-RegistryName</span></span>
<span data-ttu-id="8d07d-122">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8d07d-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="8d07d-123">-Репликация</span><span class="sxs-lookup"><span data-stu-id="8d07d-123">-Replication</span></span>
<span data-ttu-id="8d07d-124">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="8d07d-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="8d07d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d07d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d07d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d07d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="8d07d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d07d-127">-ResourceId</span></span>
<span data-ttu-id="8d07d-128">ИД ресурса репликации контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="8d07d-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="8d07d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d07d-129">-Confirm</span></span>
<span data-ttu-id="8d07d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d07d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d07d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d07d-131">-WhatIf</span></span>
<span data-ttu-id="8d07d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d07d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d07d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d07d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d07d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d07d-134">CommonParameters</span></span>
<span data-ttu-id="8d07d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d07d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d07d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d07d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d07d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d07d-137">INPUTS</span></span>

### <span data-ttu-id="8d07d-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8d07d-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="8d07d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8d07d-139">System.String</span></span>

## <span data-ttu-id="8d07d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d07d-140">OUTPUTS</span></span>

### <span data-ttu-id="8d07d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d07d-141">System.Boolean</span></span>

## <span data-ttu-id="8d07d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d07d-142">NOTES</span></span>

## <span data-ttu-id="8d07d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d07d-143">RELATED LINKS</span></span>

[<span data-ttu-id="8d07d-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8d07d-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="8d07d-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8d07d-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

