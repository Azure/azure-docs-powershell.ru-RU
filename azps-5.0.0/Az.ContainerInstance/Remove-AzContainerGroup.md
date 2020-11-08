---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248722"
---
# <span data-ttu-id="a4dcb-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a4dcb-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="a4dcb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dcb-103">Удаляет группу контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-103">Removes a container group.</span></span>

## <span data-ttu-id="a4dcb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4dcb-104">SYNTAX</span></span>

### <span data-ttu-id="a4dcb-105">RemoveContainerGroupByResourceGroupAndNameParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4dcb-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4dcb-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a4dcb-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4dcb-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a4dcb-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4dcb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dcb-108">DESCRIPTION</span></span>
<span data-ttu-id="a4dcb-109">Командлет **Remove-AzContainerGroup** удаляет группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="a4dcb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4dcb-110">EXAMPLES</span></span>

### <span data-ttu-id="a4dcb-111">Пример 1: Удаление группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="a4dcb-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="a4dcb-112">Эта команда удаляет указанную группу контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="a4dcb-113">Пример 2: Удаление группы контейнеров по конвейеру</span><span class="sxs-lookup"><span data-stu-id="a4dcb-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="a4dcb-114">Эта команда удаляет группу контейнеров по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="a4dcb-115">Пример 3: Удаление группы контейнеров по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="a4dcb-116">Эта команда удаляет группу контейнеров по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="a4dcb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4dcb-117">PARAMETERS</span></span>

### <span data-ttu-id="a4dcb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dcb-118">-DefaultProfile</span></span>
<span data-ttu-id="a4dcb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4dcb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4dcb-120">-InputObject</span></span>
<span data-ttu-id="a4dcb-121">Группа контейнера, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4dcb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4dcb-122">-Name</span></span>
<span data-ttu-id="a4dcb-123">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dcb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4dcb-124">-PassThru</span></span>
<span data-ttu-id="a4dcb-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="a4dcb-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a4dcb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dcb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4dcb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dcb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4dcb-128">-ResourceId</span></span>
<span data-ttu-id="a4dcb-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4dcb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4dcb-130">-Confirm</span></span>
<span data-ttu-id="a4dcb-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dcb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dcb-132">-WhatIf</span></span>
<span data-ttu-id="a4dcb-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dcb-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dcb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dcb-135">CommonParameters</span></span>
<span data-ttu-id="a4dcb-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4dcb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dcb-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dcb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dcb-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4dcb-138">INPUTS</span></span>

### <span data-ttu-id="a4dcb-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a4dcb-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="a4dcb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dcb-140">System.String</span></span>

## <span data-ttu-id="a4dcb-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dcb-141">OUTPUTS</span></span>

### <span data-ttu-id="a4dcb-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a4dcb-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a4dcb-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4dcb-143">NOTES</span></span>

## <span data-ttu-id="a4dcb-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4dcb-144">RELATED LINKS</span></span>
