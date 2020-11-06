---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568611"
---
# <span data-ttu-id="2800a-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2800a-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="2800a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2800a-102">SYNOPSIS</span></span>
<span data-ttu-id="2800a-103">Удаляет группу контейнера.</span><span class="sxs-lookup"><span data-stu-id="2800a-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2800a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2800a-104">SYNTAX</span></span>

### <span data-ttu-id="2800a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2800a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2800a-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="2800a-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2800a-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="2800a-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2800a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2800a-108">DESCRIPTION</span></span>
<span data-ttu-id="2800a-109">Командлет **Remove-AzureRmContainerGroup** удаляет группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2800a-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="2800a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2800a-110">EXAMPLES</span></span>

### <span data-ttu-id="2800a-111">Пример 1: Удаление группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="2800a-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="2800a-112">Эта команда удаляет указанную группу контейнера.</span><span class="sxs-lookup"><span data-stu-id="2800a-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="2800a-113">Пример 2: Удаление группы контейнеров по конвейеру</span><span class="sxs-lookup"><span data-stu-id="2800a-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="2800a-114">Эта команда удаляет группу контейнеров по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="2800a-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="2800a-115">Пример 3: Удаление группы контейнеров по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="2800a-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="2800a-116">Эта команда удаляет группу контейнеров по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="2800a-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="2800a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2800a-117">PARAMETERS</span></span>

### <span data-ttu-id="2800a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2800a-118">-DefaultProfile</span></span>
<span data-ttu-id="2800a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2800a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2800a-120">-InputObject</span></span>
<span data-ttu-id="2800a-121">Группа контейнера, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2800a-121">The container group to remove.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2800a-122">-Name</span></span>
<span data-ttu-id="2800a-123">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="2800a-123">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2800a-124">-PassThru</span></span>
<span data-ttu-id="2800a-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="2800a-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2800a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2800a-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2800a-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2800a-128">-ResourceId</span></span>
<span data-ttu-id="2800a-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2800a-129">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2800a-130">-Confirm</span></span>
<span data-ttu-id="2800a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2800a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2800a-132">-WhatIf</span></span>
<span data-ttu-id="2800a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2800a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2800a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2800a-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2800a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2800a-135">CommonParameters</span></span>
<span data-ttu-id="2800a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2800a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2800a-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2800a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2800a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2800a-138">INPUTS</span></span>

### <span data-ttu-id="2800a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2800a-139">System.String</span></span>
<span data-ttu-id="2800a-140">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2800a-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="2800a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2800a-141">OUTPUTS</span></span>

### <span data-ttu-id="2800a-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2800a-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="2800a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2800a-143">NOTES</span></span>

## <span data-ttu-id="2800a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2800a-144">RELATED LINKS</span></span>
