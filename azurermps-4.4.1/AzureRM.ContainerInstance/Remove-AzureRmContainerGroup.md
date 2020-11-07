---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: be9a289e7d3aca0bc0a4cc4e2ae8e23dbe5b1ae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733776"
---
# <span data-ttu-id="7c86f-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7c86f-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="7c86f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c86f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c86f-103">Удаляет группу контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c86f-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c86f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c86f-104">SYNTAX</span></span>

### <span data-ttu-id="7c86f-105">RemoveContainerGroupByResourceGroupAndNameParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c86f-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c86f-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7c86f-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c86f-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7c86f-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c86f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c86f-108">DESCRIPTION</span></span>
<span data-ttu-id="7c86f-109">Командлет **Remove-AzureRmContainerGroup** удаляет группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7c86f-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="7c86f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c86f-110">EXAMPLES</span></span>

### <span data-ttu-id="7c86f-111">Пример 1: Удаление группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="7c86f-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="7c86f-112">Эта команда удаляет указанную группу контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c86f-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="7c86f-113">Пример 2: Удаление группы контейнеров по конвейеру</span><span class="sxs-lookup"><span data-stu-id="7c86f-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="7c86f-114">Эта команда удаляет группу контейнеров по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="7c86f-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="7c86f-115">Пример 3: Удаление группы контейнеров по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c86f-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="7c86f-116">Эта команда удаляет группу контейнеров по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c86f-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="7c86f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c86f-117">PARAMETERS</span></span>

### <span data-ttu-id="7c86f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c86f-118">-Confirm</span></span>
<span data-ttu-id="7c86f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c86f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c86f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c86f-120">-InputObject</span></span>
<span data-ttu-id="7c86f-121">Группа контейнера, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7c86f-121">The container group to remove.</span></span>

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

### <span data-ttu-id="7c86f-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c86f-122">-Name</span></span>
<span data-ttu-id="7c86f-123">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c86f-123">The container group name.</span></span>

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

### <span data-ttu-id="7c86f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c86f-124">-PassThru</span></span>
<span data-ttu-id="7c86f-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="7c86f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7c86f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c86f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c86f-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c86f-127">The resource group name.</span></span>

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

### <span data-ttu-id="7c86f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c86f-128">-ResourceId</span></span>
<span data-ttu-id="7c86f-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c86f-129">The resource id.</span></span>

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

### <span data-ttu-id="7c86f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c86f-130">-WhatIf</span></span>
<span data-ttu-id="7c86f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c86f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c86f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c86f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c86f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c86f-133">-DefaultProfile</span></span>
<span data-ttu-id="7c86f-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c86f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c86f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c86f-135">CommonParameters</span></span>
<span data-ttu-id="7c86f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c86f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c86f-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c86f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c86f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c86f-138">INPUTS</span></span>

### <span data-ttu-id="7c86f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7c86f-139">System.String</span></span>
<span data-ttu-id="7c86f-140">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7c86f-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="7c86f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c86f-141">OUTPUTS</span></span>

### <span data-ttu-id="7c86f-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7c86f-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="7c86f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c86f-143">NOTES</span></span>

## <span data-ttu-id="7c86f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c86f-144">RELATED LINKS</span></span>

