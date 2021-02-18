---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225225"
---
# <span data-ttu-id="7f459-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7f459-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="7f459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f459-102">SYNOPSIS</span></span>
<span data-ttu-id="7f459-103">Удалить ресурс кластера.</span><span class="sxs-lookup"><span data-stu-id="7f459-103">Remove cluster resource.</span></span>

## <span data-ttu-id="7f459-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f459-104">SYNTAX</span></span>

### <span data-ttu-id="7f459-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f459-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f459-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7f459-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f459-107">ById</span><span class="sxs-lookup"><span data-stu-id="7f459-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f459-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f459-108">DESCRIPTION</span></span>
<span data-ttu-id="7f459-109">При этом будут также удаляться типы узлов под кластером.</span><span class="sxs-lookup"><span data-stu-id="7f459-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="7f459-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f459-110">EXAMPLES</span></span>

### <span data-ttu-id="7f459-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f459-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="7f459-112">"Удалить кластер".</span><span class="sxs-lookup"><span data-stu-id="7f459-112">Remove cluster.</span></span>

### <span data-ttu-id="7f459-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7f459-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="7f459-114">Удаление кластера с помощью перенастройки.</span><span class="sxs-lookup"><span data-stu-id="7f459-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="7f459-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f459-115">PARAMETERS</span></span>

### <span data-ttu-id="7f459-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f459-116">-AsJob</span></span>
<span data-ttu-id="7f459-117">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7f459-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f459-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f459-118">-DefaultProfile</span></span>
<span data-ttu-id="7f459-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f459-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f459-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f459-120">-InputObject</span></span>
<span data-ttu-id="7f459-121">Управляемый ресурс кластера</span><span class="sxs-lookup"><span data-stu-id="7f459-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f459-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7f459-122">-Name</span></span>
<span data-ttu-id="7f459-123">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="7f459-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f459-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f459-124">-PassThru</span></span>
<span data-ttu-id="7f459-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7f459-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7f459-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f459-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f459-127">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f459-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f459-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f459-128">-ResourceId</span></span>
<span data-ttu-id="7f459-129">ИД ресурсов управляемого кластера</span><span class="sxs-lookup"><span data-stu-id="7f459-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f459-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f459-130">-Confirm</span></span>
<span data-ttu-id="7f459-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f459-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f459-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f459-132">-WhatIf</span></span>
<span data-ttu-id="7f459-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f459-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f459-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f459-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f459-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f459-135">CommonParameters</span></span>
<span data-ttu-id="7f459-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f459-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f459-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f459-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f459-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f459-138">INPUTS</span></span>

### <span data-ttu-id="7f459-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7f459-139">System.String</span></span>

## <span data-ttu-id="7f459-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f459-140">OUTPUTS</span></span>

### <span data-ttu-id="7f459-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f459-141">System.Boolean</span></span>

## <span data-ttu-id="7f459-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f459-142">NOTES</span></span>

## <span data-ttu-id="7f459-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f459-143">RELATED LINKS</span></span>
