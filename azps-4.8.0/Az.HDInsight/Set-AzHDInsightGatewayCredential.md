---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 5f5c8c193a352738f64d595188247bf0564bea43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079619"
---
# <span data-ttu-id="6c6ed-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="6c6ed-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="6c6ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6ed-103">Задает учетные данные шлюза HTTP для кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6c6ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c6ed-104">SYNTAX</span></span>

### <span data-ttu-id="6c6ed-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c6ed-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c6ed-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c6ed-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c6ed-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c6ed-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c6ed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c6ed-108">DESCRIPTION</span></span>
<span data-ttu-id="6c6ed-109">Командлет **Set-AzHDInsightGatewayCredential** задает учетные данные шлюза для кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6c6ed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c6ed-110">EXAMPLES</span></span>

### <span data-ttu-id="6c6ed-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c6ed-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="6c6ed-112">Эта команда задает набор учетных данных шлюза для кластера с именем, заданным параметром-Hadoop-001 по имени.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="6c6ed-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6c6ed-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="6c6ed-114">Эта команда задает учетные данные шлюза для кластера с установленным параметром-Hadoop-001 по ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="6c6ed-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6c6ed-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="6c6ed-116">Эта команда задает учетные данные шлюза для кластера с установленным параметром "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="6c6ed-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="6c6ed-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c6ed-117">PARAMETERS</span></span>

### <span data-ttu-id="6c6ed-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c6ed-118">-AsJob</span></span>
<span data-ttu-id="6c6ed-119">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6c6ed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c6ed-120">-DefaultProfile</span></span>
<span data-ttu-id="6c6ed-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c6ed-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="6c6ed-122">-HttpCredential</span></span>
<span data-ttu-id="6c6ed-123">Возвращает или задает имя входа для пользователя кластера.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="6c6ed-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c6ed-124">-InputObject</span></span>
<span data-ttu-id="6c6ed-125">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="6c6ed-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c6ed-126">-Name</span></span>
<span data-ttu-id="6c6ed-127">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c6ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c6ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c6ed-129">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c6ed-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c6ed-130">-ResourceId</span></span>
<span data-ttu-id="6c6ed-131">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="6c6ed-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c6ed-132">-Confirm</span></span>
<span data-ttu-id="6c6ed-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c6ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c6ed-134">-WhatIf</span></span>
<span data-ttu-id="6c6ed-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c6ed-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c6ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6ed-137">CommonParameters</span></span>
<span data-ttu-id="6c6ed-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c6ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6ed-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c6ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6ed-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c6ed-140">INPUTS</span></span>

### <span data-ttu-id="6c6ed-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="6c6ed-141">None</span></span>

## <span data-ttu-id="6c6ed-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c6ed-142">OUTPUTS</span></span>

### <span data-ttu-id="6c6ed-143">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="6c6ed-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="6c6ed-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c6ed-144">NOTES</span></span>

## <span data-ttu-id="6c6ed-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c6ed-145">RELATED LINKS</span></span>