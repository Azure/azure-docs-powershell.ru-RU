---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517221"
---
# <span data-ttu-id="c04ff-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c04ff-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c04ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c04ff-103">Удалите приложение из кластера.</span><span class="sxs-lookup"><span data-stu-id="c04ff-103">Remove an application from the cluster.</span></span> <span data-ttu-id="c04ff-104">При этом будут удаляться все службы, внося в приложение.</span><span class="sxs-lookup"><span data-stu-id="c04ff-104">This will remove all the services under the application.</span></span> <span data-ttu-id="c04ff-105">Поддерживаются ARM только развернутые приложения.</span><span class="sxs-lookup"><span data-stu-id="c04ff-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="c04ff-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c04ff-106">SYNTAX</span></span>

### <span data-ttu-id="c04ff-107">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c04ff-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c04ff-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c04ff-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c04ff-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c04ff-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c04ff-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c04ff-110">DESCRIPTION</span></span>
<span data-ttu-id="c04ff-111">Этот cmdlet удаляет кластер из формы приложения.</span><span class="sxs-lookup"><span data-stu-id="c04ff-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="c04ff-112">При этом все службы, если таковые есть, удаляются из ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="c04ff-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="c04ff-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c04ff-113">EXAMPLES</span></span>

### <span data-ttu-id="c04ff-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c04ff-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="c04ff-115">В этом примере приложение testApp удаляется из группы ресурсов testRG и кластера testCluster.</span><span class="sxs-lookup"><span data-stu-id="c04ff-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="c04ff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c04ff-116">PARAMETERS</span></span>

### <span data-ttu-id="c04ff-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c04ff-117">-ClusterName</span></span>
<span data-ttu-id="c04ff-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c04ff-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c04ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04ff-119">-DefaultProfile</span></span>
<span data-ttu-id="c04ff-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c04ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c04ff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c04ff-121">-Force</span></span>
<span data-ttu-id="c04ff-122">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="c04ff-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="c04ff-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c04ff-123">-InputObject</span></span>
<span data-ttu-id="c04ff-124">Ресурс приложения.</span><span class="sxs-lookup"><span data-stu-id="c04ff-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c04ff-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c04ff-125">-Name</span></span>
<span data-ttu-id="c04ff-126">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="c04ff-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ff-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c04ff-127">-PassThru</span></span>
<span data-ttu-id="c04ff-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c04ff-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c04ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c04ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="c04ff-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c04ff-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c04ff-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c04ff-131">-ResourceId</span></span>
<span data-ttu-id="c04ff-132">Arm ResourceId приложения.</span><span class="sxs-lookup"><span data-stu-id="c04ff-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c04ff-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c04ff-133">-Confirm</span></span>
<span data-ttu-id="c04ff-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c04ff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c04ff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c04ff-135">-WhatIf</span></span>
<span data-ttu-id="c04ff-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c04ff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c04ff-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c04ff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c04ff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04ff-138">CommonParameters</span></span>
<span data-ttu-id="c04ff-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04ff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04ff-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c04ff-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04ff-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c04ff-141">INPUTS</span></span>

### <span data-ttu-id="c04ff-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c04ff-142">System.String</span></span>

### <span data-ttu-id="c04ff-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="c04ff-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c04ff-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c04ff-144">OUTPUTS</span></span>

### <span data-ttu-id="c04ff-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c04ff-145">System.Boolean</span></span>

## <span data-ttu-id="c04ff-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c04ff-146">NOTES</span></span>

## <span data-ttu-id="c04ff-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c04ff-147">RELATED LINKS</span></span>
