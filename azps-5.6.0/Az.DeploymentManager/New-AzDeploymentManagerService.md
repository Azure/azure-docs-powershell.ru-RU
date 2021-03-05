---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: b9922d84edfbf90e16db1f050ae7abaeef7442a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980723"
---
# <span data-ttu-id="de786-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="de786-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="de786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de786-102">SYNOPSIS</span></span>
<span data-ttu-id="de786-103">Создает службу в указанной топологии службы.</span><span class="sxs-lookup"><span data-stu-id="de786-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="de786-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de786-104">SYNTAX</span></span>

### <span data-ttu-id="de786-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de786-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de786-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="de786-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de786-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="de786-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de786-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de786-108">DESCRIPTION</span></span>
<span data-ttu-id="de786-109">**Cmdlet New-AzDeploymentManagerService** создает службу в топологии службы и возвращает объект, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="de786-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="de786-110">Укажите службу по имени, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de786-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="de786-111">Этот cmdlet возвращает объект Service (Служба).</span><span class="sxs-lookup"><span data-stu-id="de786-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="de786-112">Вы можете изменить этот объект локально, а затем применить изменения к службе с помощью Set-AzDeploymentManagerService-управления.</span><span class="sxs-lookup"><span data-stu-id="de786-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="de786-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de786-113">EXAMPLES</span></span>

### <span data-ttu-id="de786-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de786-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="de786-115">Создает службу с именем ContosoService1 в топологии ContosoServiceTopology группы ресурсов ContosoResourceGroup в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="de786-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="de786-116">Свойство TargetLocation указывает на то, что в указанной подписке службу ContosoService1 необходимо развернуть в восточном регионе США.</span><span class="sxs-lookup"><span data-stu-id="de786-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="de786-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de786-117">PARAMETERS</span></span>

### <span data-ttu-id="de786-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de786-118">-DefaultProfile</span></span>
<span data-ttu-id="de786-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de786-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de786-120">-Location</span><span class="sxs-lookup"><span data-stu-id="de786-120">-Location</span></span>
<span data-ttu-id="de786-121">Расположение ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="de786-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="de786-122">-Name</span><span class="sxs-lookup"><span data-stu-id="de786-122">-Name</span></span>
<span data-ttu-id="de786-123">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="de786-123">The name of the service.</span></span>

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

### <span data-ttu-id="de786-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de786-124">-ResourceGroupName</span></span>
<span data-ttu-id="de786-125">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de786-125">The resource group.</span></span>

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

### <span data-ttu-id="de786-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="de786-126">-ServiceTopologyId</span></span>
<span data-ttu-id="de786-127">Идентификатор ресурса топологии службы, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="de786-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="de786-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="de786-128">-ServiceTopologyName</span></span>
<span data-ttu-id="de786-129">Имя топологии службы, к которой относится эта служба.</span><span class="sxs-lookup"><span data-stu-id="de786-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="de786-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="de786-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="de786-131">Объект топологии службы, в котором необходимо создать службу.</span><span class="sxs-lookup"><span data-stu-id="de786-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="de786-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="de786-132">-Tag</span></span>
<span data-ttu-id="de786-133">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="de786-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="de786-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="de786-134">-TargetLocation</span></span>
<span data-ttu-id="de786-135">Определяет, куда будут развернуты ресурсы службы.</span><span class="sxs-lookup"><span data-stu-id="de786-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="de786-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de786-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="de786-137">Определяет подписку, в которую будут развернуты ресурсы службы.</span><span class="sxs-lookup"><span data-stu-id="de786-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="de786-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de786-138">-Confirm</span></span>
<span data-ttu-id="de786-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de786-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de786-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de786-140">-WhatIf</span></span>
<span data-ttu-id="de786-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de786-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de786-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="de786-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de786-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de786-143">CommonParameters</span></span>
<span data-ttu-id="de786-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de786-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de786-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de786-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de786-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de786-146">INPUTS</span></span>

### <span data-ttu-id="de786-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="de786-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de786-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de786-148">OUTPUTS</span></span>

### <span data-ttu-id="de786-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="de786-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="de786-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de786-150">NOTES</span></span>

## <span data-ttu-id="de786-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de786-151">RELATED LINKS</span></span>
