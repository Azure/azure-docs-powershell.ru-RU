---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312725"
---
# <span data-ttu-id="338de-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="338de-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="338de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="338de-102">SYNOPSIS</span></span>
<span data-ttu-id="338de-103">Создает службу для указанной топологии служб.</span><span class="sxs-lookup"><span data-stu-id="338de-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="338de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="338de-104">SYNTAX</span></span>

### <span data-ttu-id="338de-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="338de-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="338de-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="338de-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="338de-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="338de-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="338de-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="338de-108">DESCRIPTION</span></span>
<span data-ttu-id="338de-109">Командлет **New-AzDeploymentManagerService** создает службу в рамках топологии службы и возвращает объект, представляющий эту службу.</span><span class="sxs-lookup"><span data-stu-id="338de-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="338de-110">Укажите службу, указав ее имя, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="338de-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="338de-111">Командлет возвращает объект службы.</span><span class="sxs-lookup"><span data-stu-id="338de-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="338de-112">Вы можете локально изменить этот объект, а затем применить изменения к службе с помощью командлета Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="338de-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="338de-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="338de-113">EXAMPLES</span></span>

### <span data-ttu-id="338de-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="338de-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="338de-115">Создание новой службы с именем ContosoService1 в разделе "топология службы" ContosoServiceTopology в группе ресурсов "ContosoResourceGroup" в главном регионе США.</span><span class="sxs-lookup"><span data-stu-id="338de-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="338de-116">Свойство TargetLocation указывает, что служба ContosoService1 должна быть развернута в регионе "Восток США" в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="338de-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="338de-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="338de-117">PARAMETERS</span></span>

### <span data-ttu-id="338de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338de-118">-DefaultProfile</span></span>
<span data-ttu-id="338de-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="338de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338de-120">-Location</span><span class="sxs-lookup"><span data-stu-id="338de-120">-Location</span></span>
<span data-ttu-id="338de-121">Расположение ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="338de-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="338de-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="338de-122">-Name</span></span>
<span data-ttu-id="338de-123">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="338de-123">The name of the service.</span></span>

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

### <span data-ttu-id="338de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="338de-124">-ResourceGroupName</span></span>
<span data-ttu-id="338de-125">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="338de-125">The resource group.</span></span>

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

### <span data-ttu-id="338de-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="338de-126">-ServiceTopologyId</span></span>
<span data-ttu-id="338de-127">Идентификатор ресурса топологии обслуживания, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="338de-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="338de-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="338de-128">-ServiceTopologyName</span></span>
<span data-ttu-id="338de-129">Имя топологии службы, к которой принадлежит эта служба.</span><span class="sxs-lookup"><span data-stu-id="338de-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="338de-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="338de-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="338de-131">Объект Topology (топология службы), в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="338de-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="338de-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="338de-132">-Tag</span></span>
<span data-ttu-id="338de-133">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="338de-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="338de-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="338de-134">-TargetLocation</span></span>
<span data-ttu-id="338de-135">Определяет расположение, в которое должны развертываться ресурсы в службе.</span><span class="sxs-lookup"><span data-stu-id="338de-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="338de-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="338de-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="338de-137">Определяет подписку, в которой будут развернуты ресурсы в этой службе.</span><span class="sxs-lookup"><span data-stu-id="338de-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="338de-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="338de-138">-Confirm</span></span>
<span data-ttu-id="338de-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="338de-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="338de-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="338de-140">-WhatIf</span></span>
<span data-ttu-id="338de-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="338de-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="338de-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="338de-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="338de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338de-143">CommonParameters</span></span>
<span data-ttu-id="338de-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="338de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338de-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="338de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338de-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="338de-146">INPUTS</span></span>

### <span data-ttu-id="338de-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="338de-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="338de-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="338de-148">OUTPUTS</span></span>

### <span data-ttu-id="338de-149">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="338de-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="338de-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="338de-150">NOTES</span></span>

## <span data-ttu-id="338de-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="338de-151">RELATED LINKS</span></span>