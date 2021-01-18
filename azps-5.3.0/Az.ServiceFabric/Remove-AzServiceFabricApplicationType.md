---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517213"
---
# <span data-ttu-id="9b94c-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9b94c-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="9b94c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b94c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b94c-103">Удалите из кластера структуру приложения для типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9b94c-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="9b94c-104">При этом будут удаляться все версии этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b94c-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="9b94c-105">Поддерживаются только ARM развернутых типов приложений.</span><span class="sxs-lookup"><span data-stu-id="9b94c-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="9b94c-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b94c-106">SYNTAX</span></span>

### <span data-ttu-id="9b94c-107">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b94c-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b94c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b94c-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b94c-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b94c-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b94c-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b94c-110">DESCRIPTION</span></span>
<span data-ttu-id="9b94c-111">Этот командлет удаляет форму типа приложения из кластера и удаляет все версии этого ресурса, но перед запуском этой команды все приложения в нем должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="9b94c-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="9b94c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b94c-112">EXAMPLES</span></span>

### <span data-ttu-id="9b94c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b94c-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="9b94c-114">В этом примере удаляется тип testAppType приложения и все его версии.</span><span class="sxs-lookup"><span data-stu-id="9b94c-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="9b94c-115">Если есть приложения, созданные с этим типом, команда выкилает исключение.</span><span class="sxs-lookup"><span data-stu-id="9b94c-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="9b94c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b94c-116">PARAMETERS</span></span>

### <span data-ttu-id="9b94c-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9b94c-117">-ClusterName</span></span>
<span data-ttu-id="9b94c-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9b94c-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9b94c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b94c-119">-DefaultProfile</span></span>
<span data-ttu-id="9b94c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b94c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b94c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9b94c-121">-Force</span></span>
<span data-ttu-id="9b94c-122">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="9b94c-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="9b94c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b94c-123">-InputObject</span></span>
<span data-ttu-id="9b94c-124">Ресурс типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9b94c-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b94c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9b94c-125">-Name</span></span>
<span data-ttu-id="9b94c-126">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9b94c-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b94c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b94c-127">-PassThru</span></span>
<span data-ttu-id="9b94c-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9b94c-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b94c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b94c-129">-ResourceGroupName</span></span>
<span data-ttu-id="9b94c-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b94c-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9b94c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b94c-131">-ResourceId</span></span>
<span data-ttu-id="9b94c-132">Arm ResourceId типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9b94c-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="9b94c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b94c-133">-Confirm</span></span>
<span data-ttu-id="9b94c-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9b94c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b94c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b94c-135">-WhatIf</span></span>
<span data-ttu-id="9b94c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b94c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b94c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b94c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b94c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b94c-138">CommonParameters</span></span>
<span data-ttu-id="9b94c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b94c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b94c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b94c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b94c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b94c-141">INPUTS</span></span>

### <span data-ttu-id="9b94c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9b94c-142">System.String</span></span>

### <span data-ttu-id="9b94c-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="9b94c-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="9b94c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b94c-144">OUTPUTS</span></span>

### <span data-ttu-id="9b94c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b94c-145">System.Boolean</span></span>

## <span data-ttu-id="9b94c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b94c-146">NOTES</span></span>

## <span data-ttu-id="9b94c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b94c-147">RELATED LINKS</span></span>
