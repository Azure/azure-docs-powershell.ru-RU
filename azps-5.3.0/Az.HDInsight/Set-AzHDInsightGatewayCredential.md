---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504812"
---
# <span data-ttu-id="9b7eb-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="9b7eb-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="9b7eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7eb-103">Задает учетные данные шлюза HTTP в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9b7eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b7eb-104">SYNTAX</span></span>

### <span data-ttu-id="9b7eb-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b7eb-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b7eb-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b7eb-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b7eb-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b7eb-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b7eb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b7eb-108">DESCRIPTION</span></span>
<span data-ttu-id="9b7eb-109">Cmdlet **Set-AzHDInsightGatewayCredential** задает учетные данные шлюза для кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9b7eb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b7eb-110">EXAMPLES</span></span>

### <span data-ttu-id="9b7eb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b7eb-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="9b7eb-112">Эта команда задает учетные данные шлюза для кластера с именем hadoop-001 по набору параметров имени.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="9b7eb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9b7eb-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="9b7eb-114">Эта команда задает учетные данные шлюза для кластера с именем hadoop-001 by ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="9b7eb-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9b7eb-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="9b7eb-116">Эта команда задает учетные данные шлюза для кластера с именем hadoop-001 by InputObject.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="9b7eb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b7eb-117">PARAMETERS</span></span>

### <span data-ttu-id="9b7eb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b7eb-118">-AsJob</span></span>
<span data-ttu-id="9b7eb-119">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9b7eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7eb-120">-DefaultProfile</span></span>
<span data-ttu-id="9b7eb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b7eb-122">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="9b7eb-122">-HttpCredential</span></span>
<span data-ttu-id="9b7eb-123">Возвращает или устанавливает вход для пользователя кластера.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7eb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b7eb-124">-InputObject</span></span>
<span data-ttu-id="9b7eb-125">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7eb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9b7eb-126">-Name</span></span>
<span data-ttu-id="9b7eb-127">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b7eb-129">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7eb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b7eb-130">-ResourceId</span></span>
<span data-ttu-id="9b7eb-131">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7eb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b7eb-132">-Confirm</span></span>
<span data-ttu-id="9b7eb-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7eb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7eb-134">-WhatIf</span></span>
<span data-ttu-id="9b7eb-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b7eb-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7eb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7eb-137">CommonParameters</span></span>
<span data-ttu-id="9b7eb-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7eb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7eb-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b7eb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7eb-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b7eb-140">INPUTS</span></span>

### <span data-ttu-id="9b7eb-141">Нет</span><span class="sxs-lookup"><span data-stu-id="9b7eb-141">None</span></span>

## <span data-ttu-id="9b7eb-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b7eb-142">OUTPUTS</span></span>

### <span data-ttu-id="9b7eb-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="9b7eb-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="9b7eb-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b7eb-144">NOTES</span></span>

## <span data-ttu-id="9b7eb-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b7eb-145">RELATED LINKS</span></span>
