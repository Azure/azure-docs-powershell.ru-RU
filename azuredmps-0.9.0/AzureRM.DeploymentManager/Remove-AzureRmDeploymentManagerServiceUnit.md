---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556087"
---
# <span data-ttu-id="b3266-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3266-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="b3266-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3266-102">SYNOPSIS</span></span>
<span data-ttu-id="b3266-103">Удаляет модуль службы в топологии службы.</span><span class="sxs-lookup"><span data-stu-id="b3266-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="b3266-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3266-104">SYNTAX</span></span>

### <span data-ttu-id="b3266-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3266-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3266-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b3266-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3266-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b3266-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3266-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="b3266-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3266-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b3266-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3266-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3266-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3266-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="b3266-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3266-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3266-112">DESCRIPTION</span></span>
<span data-ttu-id="b3266-113">Командлет **Remove-AzureRmDeploymentManagerServiceUnit** удаляет модуль службы в службе.</span><span class="sxs-lookup"><span data-stu-id="b3266-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="b3266-114">Укажите модуль обслуживания по ее имени, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3266-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="b3266-115">Кроме того, можно предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b3266-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="b3266-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3266-116">EXAMPLES</span></span>

### <span data-ttu-id="b3266-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3266-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="b3266-118">Эта команда удаляет модуль служб с именем ContosoService1Storage в службе ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b3266-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b3266-119">Пример 2: удаление единицы обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3266-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="b3266-120">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b3266-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b3266-121">Пример 3: удаление единицы обслуживания с помощью объекта сервисного модуля.</span><span class="sxs-lookup"><span data-stu-id="b3266-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="b3266-122">Эта команда удаляет сервисный модуль с именем, именем службы, именем и $serviceUnitObject свойством ResourceGroup для службы Name, ServiceName, ServiceTopologyName и ResourceGroupName, соответственно.</span><span class="sxs-lookup"><span data-stu-id="b3266-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="b3266-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3266-123">PARAMETERS</span></span>

### <span data-ttu-id="b3266-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3266-124">-DefaultProfile</span></span>
<span data-ttu-id="b3266-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3266-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3266-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b3266-126">-Force</span></span>
<span data-ttu-id="b3266-127">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b3266-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b3266-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3266-128">-Name</span></span>
<span data-ttu-id="b3266-129">Имя единицы услуги, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b3266-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3266-130">-PassThru</span></span>
<span data-ttu-id="b3266-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="b3266-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b3266-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3266-132">-ResourceGroupName</span></span>
<span data-ttu-id="b3266-133">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3266-133">The resource group.</span></span>

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

### <span data-ttu-id="b3266-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3266-134">-ResourceId</span></span>
<span data-ttu-id="b3266-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3266-135">The resource identifier.</span></span>

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

### <span data-ttu-id="b3266-136">-Служба</span><span class="sxs-lookup"><span data-stu-id="b3266-136">-Service</span></span>
<span data-ttu-id="b3266-137">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3266-137">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b3266-138">-ServiceName</span></span>
<span data-ttu-id="b3266-139">Имя службы, к которой относится модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3266-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b3266-140">-ServiceResourceId</span></span>
<span data-ttu-id="b3266-141">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3266-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b3266-142">-ServiceTopology</span></span>
<span data-ttu-id="b3266-143">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3266-143">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="b3266-144">-ServiceTopologyName</span></span>
<span data-ttu-id="b3266-145">Имя топологии обслуживания, к которой относится модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3266-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="b3266-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b3266-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b3266-147">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3266-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3266-148">-ServiceUnit</span></span>
<span data-ttu-id="b3266-149">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b3266-149">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3266-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3266-150">-Confirm</span></span>
<span data-ttu-id="b3266-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3266-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3266-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3266-152">-WhatIf</span></span>
<span data-ttu-id="b3266-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3266-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3266-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3266-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3266-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3266-155">CommonParameters</span></span>
<span data-ttu-id="b3266-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3266-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3266-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3266-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3266-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3266-158">INPUTS</span></span>

### <span data-ttu-id="b3266-159">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="b3266-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b3266-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3266-160">OUTPUTS</span></span>

### <span data-ttu-id="b3266-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3266-161">System.Boolean</span></span>

## <span data-ttu-id="b3266-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3266-162">NOTES</span></span>

## <span data-ttu-id="b3266-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3266-163">RELATED LINKS</span></span>

[<span data-ttu-id="b3266-164">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3266-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b3266-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3266-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b3266-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3266-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)