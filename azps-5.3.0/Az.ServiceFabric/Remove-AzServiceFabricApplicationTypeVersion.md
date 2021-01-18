---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517226"
---
# <span data-ttu-id="2f2a5-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2f2a5-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="2f2a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2a5-103">Удалите из кластера структуру приложения версии приложения.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="2f2a5-104">Поддерживаются только ARM развернутые версии приложений.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="2f2a5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f2a5-105">SYNTAX</span></span>

### <span data-ttu-id="2f2a5-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f2a5-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f2a5-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2a5-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f2a5-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f2a5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f2a5-109">DESCRIPTION</span></span>
<span data-ttu-id="2f2a5-110">Этот cmdlet remove Service fabric an application version from the cluster.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="2f2a5-111">Перед запуском этой команды необходимо удалить все приложения этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="2f2a5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f2a5-112">EXAMPLES</span></span>

### <span data-ttu-id="2f2a5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f2a5-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="2f2a5-114">В этом примере версия v1 удаляется под типом testAppType.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="2f2a5-115">В этом ресурсе есть все приложения, команда выкинуть исключение.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="2f2a5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f2a5-116">PARAMETERS</span></span>

### <span data-ttu-id="2f2a5-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2f2a5-117">-ClusterName</span></span>
<span data-ttu-id="2f2a5-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2f2a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2a5-119">-DefaultProfile</span></span>
<span data-ttu-id="2f2a5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f2a5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2f2a5-121">-Force</span></span>
<span data-ttu-id="2f2a5-122">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="2f2a5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f2a5-123">-InputObject</span></span>
<span data-ttu-id="2f2a5-124">Ресурс версии приложения.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2f2a5-125">-Name</span></span>
<span data-ttu-id="2f2a5-126">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f2a5-127">-PassThru</span></span>
<span data-ttu-id="2f2a5-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2f2a5-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f2a5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2a5-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f2a5-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2f2a5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f2a5-131">-ResourceId</span></span>
<span data-ttu-id="2f2a5-132">Arm ResourceId версии приложения.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="2f2a5-133">-Версия</span><span class="sxs-lookup"><span data-stu-id="2f2a5-133">-Version</span></span>
<span data-ttu-id="2f2a5-134">Укажите версию типа приложения.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2a5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f2a5-135">-Confirm</span></span>
<span data-ttu-id="2f2a5-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f2a5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f2a5-137">-WhatIf</span></span>
<span data-ttu-id="2f2a5-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f2a5-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f2a5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2a5-140">CommonParameters</span></span>
<span data-ttu-id="2f2a5-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2a5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2a5-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f2a5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2a5-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f2a5-143">INPUTS</span></span>

### <span data-ttu-id="2f2a5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2f2a5-144">System.String</span></span>

### <span data-ttu-id="2f2a5-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2f2a5-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="2f2a5-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f2a5-146">OUTPUTS</span></span>

### <span data-ttu-id="2f2a5-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f2a5-147">System.Boolean</span></span>

## <span data-ttu-id="2f2a5-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f2a5-148">NOTES</span></span>

## <span data-ttu-id="2f2a5-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f2a5-149">RELATED LINKS</span></span>
