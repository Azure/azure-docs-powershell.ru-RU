---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555308"
---
# <span data-ttu-id="15c8d-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="15c8d-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="15c8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="15c8d-103">Удаляет службу из топологии служб.</span><span class="sxs-lookup"><span data-stu-id="15c8d-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="15c8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15c8d-104">SYNTAX</span></span>

### <span data-ttu-id="15c8d-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15c8d-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15c8d-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="15c8d-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c8d-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="15c8d-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c8d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="15c8d-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c8d-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="15c8d-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c8d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15c8d-110">DESCRIPTION</span></span>
<span data-ttu-id="15c8d-111">Командлет **Remove-AzureRmDeploymentManagerService** Удаляет службу из топологии служб.</span><span class="sxs-lookup"><span data-stu-id="15c8d-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="15c8d-112">Укажите службу, указав ее имя, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15c8d-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="15c8d-113">Кроме того, можно предоставить объект обслуживания или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="15c8d-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="15c8d-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15c8d-114">EXAMPLES</span></span>

### <span data-ttu-id="15c8d-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15c8d-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="15c8d-116">Эта команда удаляет службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="15c8d-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="15c8d-117">Пример 2: Удаление службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="15c8d-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="15c8d-118">Эта команда удаляет службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="15c8d-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="15c8d-119">Пример 3: Удаление службы с помощью объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="15c8d-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="15c8d-120">Эта команда удаляет службу, имя которой, имя топологии службы и ResourceGroup, совпадают со свойствами Name, ServiceTopologyName и ResourceGroupName для $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="15c8d-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="15c8d-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15c8d-121">PARAMETERS</span></span>

### <span data-ttu-id="15c8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c8d-122">-DefaultProfile</span></span>
<span data-ttu-id="15c8d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15c8d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c8d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="15c8d-124">-Force</span></span>
<span data-ttu-id="15c8d-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="15c8d-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="15c8d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15c8d-126">-Name</span></span>
<span data-ttu-id="15c8d-127">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="15c8d-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c8d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15c8d-128">-PassThru</span></span>
<span data-ttu-id="15c8d-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="15c8d-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="15c8d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c8d-130">-ResourceGroupName</span></span>
<span data-ttu-id="15c8d-131">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15c8d-131">The resource group.</span></span>

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

### <span data-ttu-id="15c8d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15c8d-132">-ResourceId</span></span>
<span data-ttu-id="15c8d-133">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="15c8d-133">The resource identifier.</span></span>

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

### <span data-ttu-id="15c8d-134">-Служба</span><span class="sxs-lookup"><span data-stu-id="15c8d-134">-Service</span></span>
<span data-ttu-id="15c8d-135">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="15c8d-135">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c8d-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="15c8d-136">-ServiceTopology</span></span>
<span data-ttu-id="15c8d-137">Объект Topology (топология службы), в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="15c8d-137">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c8d-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="15c8d-138">-ServiceTopologyName</span></span>
<span data-ttu-id="15c8d-139">Имя топологии службы, к которой принадлежит служба.</span><span class="sxs-lookup"><span data-stu-id="15c8d-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="15c8d-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="15c8d-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="15c8d-141">Идентификатор ресурса топологии обслуживания, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="15c8d-141">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c8d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15c8d-142">-Confirm</span></span>
<span data-ttu-id="15c8d-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15c8d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c8d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c8d-144">-WhatIf</span></span>
<span data-ttu-id="15c8d-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15c8d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c8d-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15c8d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c8d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c8d-147">CommonParameters</span></span>
<span data-ttu-id="15c8d-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15c8d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c8d-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c8d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c8d-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15c8d-150">INPUTS</span></span>

### <span data-ttu-id="15c8d-151">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="15c8d-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="15c8d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15c8d-152">OUTPUTS</span></span>

### <span data-ttu-id="15c8d-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15c8d-153">System.Boolean</span></span>

## <span data-ttu-id="15c8d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="15c8d-154">NOTES</span></span>

## <span data-ttu-id="15c8d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15c8d-155">RELATED LINKS</span></span>

[<span data-ttu-id="15c8d-156">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="15c8d-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="15c8d-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="15c8d-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="15c8d-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="15c8d-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)