---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517185"
---
# <span data-ttu-id="a60b0-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a60b0-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="a60b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a60b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a60b0-103">Удалите службу из кластера.</span><span class="sxs-lookup"><span data-stu-id="a60b0-103">Remove a service from the cluster.</span></span> <span data-ttu-id="a60b0-104">Поддерживаются только ARM развернутые службы.</span><span class="sxs-lookup"><span data-stu-id="a60b0-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="a60b0-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a60b0-105">SYNTAX</span></span>

### <span data-ttu-id="a60b0-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a60b0-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a60b0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a60b0-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60b0-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a60b0-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60b0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a60b0-109">DESCRIPTION</span></span>
<span data-ttu-id="a60b0-110">Этот cmdlet removes a service form the cluster.</span><span class="sxs-lookup"><span data-stu-id="a60b0-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="a60b0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a60b0-111">EXAMPLES</span></span>

### <span data-ttu-id="a60b0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a60b0-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="a60b0-113">В этом примере удаляется служба testApp~testService1.</span><span class="sxs-lookup"><span data-stu-id="a60b0-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="a60b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a60b0-114">PARAMETERS</span></span>

### <span data-ttu-id="a60b0-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a60b0-115">-ApplicationName</span></span>
<span data-ttu-id="a60b0-116">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="a60b0-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60b0-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a60b0-117">-ClusterName</span></span>
<span data-ttu-id="a60b0-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="a60b0-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60b0-119">-DefaultProfile</span></span>
<span data-ttu-id="a60b0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a60b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a60b0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a60b0-121">-Force</span></span>
<span data-ttu-id="a60b0-122">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="a60b0-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="a60b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a60b0-123">-InputObject</span></span>
<span data-ttu-id="a60b0-124">Ресурс службы.</span><span class="sxs-lookup"><span data-stu-id="a60b0-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a60b0-125">-Name</span></span>
<span data-ttu-id="a60b0-126">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="a60b0-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60b0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a60b0-127">-PassThru</span></span>
<span data-ttu-id="a60b0-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a60b0-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a60b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="a60b0-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a60b0-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a60b0-131">-ResourceId</span></span>
<span data-ttu-id="a60b0-132">Arm ResourceId службы.</span><span class="sxs-lookup"><span data-stu-id="a60b0-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a60b0-133">-Confirm</span></span>
<span data-ttu-id="a60b0-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60b0-135">-WhatIf</span></span>
<span data-ttu-id="a60b0-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a60b0-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a60b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60b0-138">CommonParameters</span></span>
<span data-ttu-id="a60b0-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60b0-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a60b0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60b0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a60b0-141">INPUTS</span></span>

### <span data-ttu-id="a60b0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a60b0-142">System.String</span></span>

### <span data-ttu-id="a60b0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="a60b0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="a60b0-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a60b0-144">OUTPUTS</span></span>

### <span data-ttu-id="a60b0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a60b0-145">System.Boolean</span></span>

## <span data-ttu-id="a60b0-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a60b0-146">NOTES</span></span>

## <span data-ttu-id="a60b0-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a60b0-147">RELATED LINKS</span></span>
