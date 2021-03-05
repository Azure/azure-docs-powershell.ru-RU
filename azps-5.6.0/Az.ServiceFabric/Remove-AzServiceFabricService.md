---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 992cd2a381e9eda89b9388ec1ed37f74a76e9adf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005416"
---
# <span data-ttu-id="27db3-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="27db3-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="27db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27db3-102">SYNOPSIS</span></span>
<span data-ttu-id="27db3-103">Удалите службу из кластера.</span><span class="sxs-lookup"><span data-stu-id="27db3-103">Remove a service from the cluster.</span></span> <span data-ttu-id="27db3-104">Поддерживаются только ARM развернутые службы.</span><span class="sxs-lookup"><span data-stu-id="27db3-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="27db3-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27db3-105">SYNTAX</span></span>

### <span data-ttu-id="27db3-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27db3-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27db3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27db3-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27db3-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27db3-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27db3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27db3-109">DESCRIPTION</span></span>
<span data-ttu-id="27db3-110">Этот cmdlet removes a service form the cluster.</span><span class="sxs-lookup"><span data-stu-id="27db3-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="27db3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27db3-111">EXAMPLES</span></span>

### <span data-ttu-id="27db3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27db3-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="27db3-113">В этом примере удаляется служба testApp~testService1.</span><span class="sxs-lookup"><span data-stu-id="27db3-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="27db3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27db3-114">PARAMETERS</span></span>

### <span data-ttu-id="27db3-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="27db3-115">-ApplicationName</span></span>
<span data-ttu-id="27db3-116">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="27db3-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="27db3-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="27db3-117">-ClusterName</span></span>
<span data-ttu-id="27db3-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="27db3-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="27db3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27db3-119">-DefaultProfile</span></span>
<span data-ttu-id="27db3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27db3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27db3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="27db3-121">-Force</span></span>
<span data-ttu-id="27db3-122">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="27db3-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="27db3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27db3-123">-InputObject</span></span>
<span data-ttu-id="27db3-124">Ресурс службы.</span><span class="sxs-lookup"><span data-stu-id="27db3-124">The service resource.</span></span>

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

### <span data-ttu-id="27db3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="27db3-125">-Name</span></span>
<span data-ttu-id="27db3-126">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="27db3-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="27db3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27db3-127">-PassThru</span></span>
<span data-ttu-id="27db3-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="27db3-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="27db3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27db3-129">-ResourceGroupName</span></span>
<span data-ttu-id="27db3-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27db3-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="27db3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27db3-131">-ResourceId</span></span>
<span data-ttu-id="27db3-132">Arm ResourceId службы.</span><span class="sxs-lookup"><span data-stu-id="27db3-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="27db3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27db3-133">-Confirm</span></span>
<span data-ttu-id="27db3-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27db3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27db3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27db3-135">-WhatIf</span></span>
<span data-ttu-id="27db3-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27db3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27db3-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="27db3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27db3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27db3-138">CommonParameters</span></span>
<span data-ttu-id="27db3-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27db3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27db3-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27db3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27db3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27db3-141">INPUTS</span></span>

### <span data-ttu-id="27db3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="27db3-142">System.String</span></span>

### <span data-ttu-id="27db3-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="27db3-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="27db3-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27db3-144">OUTPUTS</span></span>

### <span data-ttu-id="27db3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27db3-145">System.Boolean</span></span>

## <span data-ttu-id="27db3-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27db3-146">NOTES</span></span>

## <span data-ttu-id="27db3-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27db3-147">RELATED LINKS</span></span>
