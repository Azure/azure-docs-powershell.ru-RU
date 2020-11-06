---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555392"
---
# <span data-ttu-id="c2eee-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c2eee-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="c2eee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2eee-102">SYNOPSIS</span></span>
<span data-ttu-id="c2eee-103">Удаление топологии службы и всех ее ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2eee-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="c2eee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2eee-104">SYNTAX</span></span>

### <span data-ttu-id="c2eee-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2eee-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2eee-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2eee-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2eee-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c2eee-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2eee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2eee-108">DESCRIPTION</span></span>
<span data-ttu-id="c2eee-109">Командлет **Remove-AzureRmDeploymentManagerServiceTopology** удаляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="c2eee-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="c2eee-110">Укажите топологию службы по ее имени и названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2eee-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="c2eee-111">Кроме того, можно предоставить объект ServiceTopology или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c2eee-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="c2eee-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2eee-112">EXAMPLES</span></span>

### <span data-ttu-id="c2eee-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2eee-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="c2eee-114">Эта команда удаляет из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c2eee-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2eee-115">Пример 2. Удалите топологию службы, используя идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2eee-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="c2eee-116">Эта команда удаляет из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c2eee-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2eee-117">Пример 3: Удаление топологии служб с помощью объекта Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="c2eee-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="c2eee-118">Эта команда удаляет топологию службы, имя и название ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="c2eee-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="c2eee-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2eee-119">PARAMETERS</span></span>

### <span data-ttu-id="c2eee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2eee-120">-DefaultProfile</span></span>
<span data-ttu-id="c2eee-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2eee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2eee-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c2eee-122">-Force</span></span>
<span data-ttu-id="c2eee-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c2eee-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c2eee-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2eee-124">-Name</span></span>
<span data-ttu-id="c2eee-125">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="c2eee-125">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eee-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2eee-126">-PassThru</span></span>
<span data-ttu-id="c2eee-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="c2eee-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2eee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2eee-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2eee-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2eee-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2eee-130">-ResourceId</span></span>
<span data-ttu-id="c2eee-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2eee-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eee-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c2eee-132">-ServiceTopology</span></span>
<span data-ttu-id="c2eee-133">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c2eee-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eee-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2eee-134">-Confirm</span></span>
<span data-ttu-id="c2eee-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2eee-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2eee-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2eee-136">-WhatIf</span></span>
<span data-ttu-id="c2eee-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2eee-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2eee-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2eee-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2eee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2eee-139">CommonParameters</span></span>
<span data-ttu-id="c2eee-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2eee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2eee-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2eee-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2eee-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2eee-142">INPUTS</span></span>

### <span data-ttu-id="c2eee-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c2eee-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c2eee-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2eee-144">OUTPUTS</span></span>

### <span data-ttu-id="c2eee-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2eee-145">System.Boolean</span></span>

## <span data-ttu-id="c2eee-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2eee-146">NOTES</span></span>

## <span data-ttu-id="c2eee-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2eee-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2eee-148">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c2eee-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="c2eee-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c2eee-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="c2eee-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c2eee-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)