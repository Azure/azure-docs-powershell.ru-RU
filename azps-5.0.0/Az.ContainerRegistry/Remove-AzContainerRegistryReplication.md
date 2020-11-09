---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311855"
---
# <span data-ttu-id="d696a-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d696a-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="d696a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d696a-102">SYNOPSIS</span></span>
<span data-ttu-id="d696a-103">Удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="d696a-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="d696a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d696a-104">SYNTAX</span></span>

### <span data-ttu-id="d696a-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d696a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d696a-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d696a-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d696a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d696a-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d696a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d696a-108">DESCRIPTION</span></span>
<span data-ttu-id="d696a-109">Командлет Remove-AzContainerRegistryReplication удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="d696a-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="d696a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d696a-110">EXAMPLES</span></span>

### <span data-ttu-id="d696a-111">Пример 1: удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="d696a-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="d696a-112">Удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="d696a-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="d696a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d696a-113">PARAMETERS</span></span>

### <span data-ttu-id="d696a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d696a-114">-DefaultProfile</span></span>
<span data-ttu-id="d696a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d696a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d696a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d696a-116">-Name</span></span>
<span data-ttu-id="d696a-117">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="d696a-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="d696a-118">По умолчанию — имя расположения.</span><span class="sxs-lookup"><span data-stu-id="d696a-118">Default to the location name.</span></span>

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

### <span data-ttu-id="d696a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d696a-119">-PassThru</span></span>
<span data-ttu-id="d696a-120">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="d696a-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="d696a-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d696a-121">-RegistryName</span></span>
<span data-ttu-id="d696a-122">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="d696a-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="d696a-123">-Репликация</span><span class="sxs-lookup"><span data-stu-id="d696a-123">-Replication</span></span>
<span data-ttu-id="d696a-124">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="d696a-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="d696a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d696a-125">-ResourceGroupName</span></span>
<span data-ttu-id="d696a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d696a-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="d696a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d696a-127">-ResourceId</span></span>
<span data-ttu-id="d696a-128">Идентификатор ресурса репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="d696a-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="d696a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d696a-129">-Confirm</span></span>
<span data-ttu-id="d696a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d696a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d696a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d696a-131">-WhatIf</span></span>
<span data-ttu-id="d696a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d696a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d696a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d696a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d696a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d696a-134">CommonParameters</span></span>
<span data-ttu-id="d696a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d696a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d696a-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d696a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d696a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d696a-137">INPUTS</span></span>

### <span data-ttu-id="d696a-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d696a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="d696a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d696a-139">System.String</span></span>

## <span data-ttu-id="d696a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d696a-140">OUTPUTS</span></span>

### <span data-ttu-id="d696a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d696a-141">System.Boolean</span></span>

## <span data-ttu-id="d696a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d696a-142">NOTES</span></span>

## <span data-ttu-id="d696a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d696a-143">RELATED LINKS</span></span>

[<span data-ttu-id="d696a-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d696a-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="d696a-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d696a-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

