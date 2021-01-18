---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507597"
---
# <span data-ttu-id="cbfaf-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="cbfaf-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="cbfaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfaf-103">Создает службу в указанной топологии службы.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="cbfaf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cbfaf-104">SYNTAX</span></span>

### <span data-ttu-id="cbfaf-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbfaf-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbfaf-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="cbfaf-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbfaf-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="cbfaf-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbfaf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbfaf-108">DESCRIPTION</span></span>
<span data-ttu-id="cbfaf-109">**Cmdlet New-AzDeploymentManagerService** создает службу в топологии службы и возвращает объект, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="cbfaf-110">Укажите службу по имени, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="cbfaf-111">Этот cmdlet возвращает объект Service (Служба).</span><span class="sxs-lookup"><span data-stu-id="cbfaf-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="cbfaf-112">Вы можете изменить этот объект локально, а затем применить изменения к службе с помощью Set-AzDeploymentManagerService-управления.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="cbfaf-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cbfaf-113">EXAMPLES</span></span>

### <span data-ttu-id="cbfaf-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cbfaf-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="cbfaf-115">Создает службу с именем ContosoService1 в топологии ContosoServiceTopology группы ресурсов ContosoResourceGroup в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="cbfaf-116">Свойство TargetLocation указывает на то, что в указанной подписке службу ContosoService1 необходимо развернуть в восточном регионе США.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="cbfaf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbfaf-117">PARAMETERS</span></span>

### <span data-ttu-id="cbfaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfaf-118">-DefaultProfile</span></span>
<span data-ttu-id="cbfaf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbfaf-120">-Location</span><span class="sxs-lookup"><span data-stu-id="cbfaf-120">-Location</span></span>
<span data-ttu-id="cbfaf-121">Расположение ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cbfaf-122">-Name</span></span>
<span data-ttu-id="cbfaf-123">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbfaf-124">-ResourceGroupName</span></span>
<span data-ttu-id="cbfaf-125">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="cbfaf-126">-ServiceTopologyId</span></span>
<span data-ttu-id="cbfaf-127">Идентификатор ресурса топологии службы, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="cbfaf-128">-ServiceTopologyName</span></span>
<span data-ttu-id="cbfaf-129">Имя топологии службы, к которой относится эта служба.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="cbfaf-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="cbfaf-131">Объект топологии службы, в котором необходимо создать службу.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="cbfaf-132">-Tag</span></span>
<span data-ttu-id="cbfaf-133">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="cbfaf-134">-TargetLocation</span></span>
<span data-ttu-id="cbfaf-135">Определяет, куда будут развернуты ресурсы службы.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbfaf-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="cbfaf-137">Определяет подписку, в которую будут развернуты ресурсы службы.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfaf-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbfaf-138">-Confirm</span></span>
<span data-ttu-id="cbfaf-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbfaf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbfaf-140">-WhatIf</span></span>
<span data-ttu-id="cbfaf-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbfaf-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbfaf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfaf-143">CommonParameters</span></span>
<span data-ttu-id="cbfaf-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbfaf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfaf-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbfaf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfaf-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbfaf-146">INPUTS</span></span>

### <span data-ttu-id="cbfaf-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cbfaf-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cbfaf-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cbfaf-148">OUTPUTS</span></span>

### <span data-ttu-id="cbfaf-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="cbfaf-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="cbfaf-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cbfaf-150">NOTES</span></span>

## <span data-ttu-id="cbfaf-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbfaf-151">RELATED LINKS</span></span>
