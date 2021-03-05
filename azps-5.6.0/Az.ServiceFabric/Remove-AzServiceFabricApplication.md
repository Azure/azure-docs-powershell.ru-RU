---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 5004b6b9528eb91a1883805405dba6147d5161a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005587"
---
# <span data-ttu-id="d738b-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d738b-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="d738b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d738b-102">SYNOPSIS</span></span>
<span data-ttu-id="d738b-103">Удалите приложение из кластера.</span><span class="sxs-lookup"><span data-stu-id="d738b-103">Remove an application from the cluster.</span></span> <span data-ttu-id="d738b-104">При этом будут удалиться все службы, внося в приложение.</span><span class="sxs-lookup"><span data-stu-id="d738b-104">This will remove all the services under the application.</span></span> <span data-ttu-id="d738b-105">Поддерживаются ARM только развернутые приложения.</span><span class="sxs-lookup"><span data-stu-id="d738b-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="d738b-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d738b-106">SYNTAX</span></span>

### <span data-ttu-id="d738b-107">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d738b-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d738b-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d738b-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d738b-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d738b-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d738b-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d738b-110">DESCRIPTION</span></span>
<span data-ttu-id="d738b-111">Этот cmdlet удаляет кластер из формы приложения.</span><span class="sxs-lookup"><span data-stu-id="d738b-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="d738b-112">При этом все службы, если таковые есть, удаляются из ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="d738b-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="d738b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d738b-113">EXAMPLES</span></span>

### <span data-ttu-id="d738b-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d738b-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="d738b-115">В этом примере приложение testApp удаляется из группы ресурсов testRG и кластера testCluster.</span><span class="sxs-lookup"><span data-stu-id="d738b-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="d738b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d738b-116">PARAMETERS</span></span>

### <span data-ttu-id="d738b-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d738b-117">-ClusterName</span></span>
<span data-ttu-id="d738b-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="d738b-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d738b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d738b-119">-DefaultProfile</span></span>
<span data-ttu-id="d738b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d738b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d738b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d738b-121">-Force</span></span>
<span data-ttu-id="d738b-122">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="d738b-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="d738b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d738b-123">-InputObject</span></span>
<span data-ttu-id="d738b-124">Ресурс приложения.</span><span class="sxs-lookup"><span data-stu-id="d738b-124">The application resource.</span></span>

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

### <span data-ttu-id="d738b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d738b-125">-Name</span></span>
<span data-ttu-id="d738b-126">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="d738b-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="d738b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d738b-127">-PassThru</span></span>
<span data-ttu-id="d738b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d738b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d738b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d738b-129">-ResourceGroupName</span></span>
<span data-ttu-id="d738b-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d738b-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d738b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d738b-131">-ResourceId</span></span>
<span data-ttu-id="d738b-132">Arm ResourceId приложения.</span><span class="sxs-lookup"><span data-stu-id="d738b-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="d738b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d738b-133">-Confirm</span></span>
<span data-ttu-id="d738b-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d738b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d738b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d738b-135">-WhatIf</span></span>
<span data-ttu-id="d738b-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d738b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d738b-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d738b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d738b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d738b-138">CommonParameters</span></span>
<span data-ttu-id="d738b-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d738b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d738b-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d738b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d738b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d738b-141">INPUTS</span></span>

### <span data-ttu-id="d738b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d738b-142">System.String</span></span>

### <span data-ttu-id="d738b-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="d738b-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d738b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d738b-144">OUTPUTS</span></span>

### <span data-ttu-id="d738b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d738b-145">System.Boolean</span></span>

## <span data-ttu-id="d738b-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d738b-146">NOTES</span></span>

## <span data-ttu-id="d738b-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d738b-147">RELATED LINKS</span></span>
