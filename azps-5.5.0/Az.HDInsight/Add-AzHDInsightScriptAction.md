---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: 2759059da9bc37f942eaa733319539bc1fa53b5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219972"
---
# <span data-ttu-id="56f32-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="56f32-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="56f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f32-102">SYNOPSIS</span></span>
<span data-ttu-id="56f32-103">Добавляет действие сценария к объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="56f32-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="56f32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56f32-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f32-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56f32-105">DESCRIPTION</span></span>
<span data-ttu-id="56f32-106">Для объекта конфигурации HDInsight, созданного New-AzHDInsightClusterConfig HDInsight, добавляются действия сценария **Add-AzHDInsightScriptAction.**</span><span class="sxs-lookup"><span data-stu-id="56f32-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="56f32-107">Действия сценария предоставляют функции, которые используются для установки дополнительного программного обеспечения или изменения конфигурации приложений, которые запускаются на кластере Hadoop с помощью сценариев Windows PowerShell или Bash (для кластеров Windows или Linux соответственно).</span><span class="sxs-lookup"><span data-stu-id="56f32-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="56f32-108">На узлах кластера выполняется действие сценария при развертывании кластеров HDInsight и после узлов в конфигурации HDInsight кластера.</span><span class="sxs-lookup"><span data-stu-id="56f32-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="56f32-109">Сценарий выполняется в соответствии с правами учетной записи администратора и предоставляет полные права доступа к узлам кластера.</span><span class="sxs-lookup"><span data-stu-id="56f32-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="56f32-110">Вы можете предоставить каждому кластеру список действий сценариев, которые должны запускаться в указанной последовательности.</span><span class="sxs-lookup"><span data-stu-id="56f32-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="56f32-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56f32-111">EXAMPLES</span></span>

### <span data-ttu-id="56f32-112">Пример 1. Добавление действия сценария к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="56f32-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="56f32-113">Эта команда добавляет действие сценария для узлов "Руководитель и работник" кластера hadoop-001, которые будут запускаться в конце создания кластера.</span><span class="sxs-lookup"><span data-stu-id="56f32-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="56f32-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56f32-114">PARAMETERS</span></span>

### <span data-ttu-id="56f32-115">-Config</span><span class="sxs-lookup"><span data-stu-id="56f32-115">-Config</span></span>
<span data-ttu-id="56f32-116">Определяет объект конфигурации кластера HDInsight, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56f32-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="56f32-117">Этот объект создается с помощью **командылета New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="56f32-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56f32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f32-118">-DefaultProfile</span></span>
<span data-ttu-id="56f32-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="56f32-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56f32-120">-Name</span><span class="sxs-lookup"><span data-stu-id="56f32-120">-Name</span></span>
<span data-ttu-id="56f32-121">Указывает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="56f32-121">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f32-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="56f32-122">-NodeType</span></span>
<span data-ttu-id="56f32-123">Указывает тип узла, для которого нужно выполнить действие сценария.</span><span class="sxs-lookup"><span data-stu-id="56f32-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="56f32-124">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="56f32-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f32-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="56f32-125">HeadNode</span></span>
- <span data-ttu-id="56f32-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="56f32-126">WorkerNode</span></span>
- <span data-ttu-id="56f32-127">Разномер</span><span class="sxs-lookup"><span data-stu-id="56f32-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f32-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="56f32-128">-Parameters</span></span>
<span data-ttu-id="56f32-129">Определяет параметры для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="56f32-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f32-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="56f32-130">-Uri</span></span>
<span data-ttu-id="56f32-131">Указывает общедоступный URI для действия сценария (сценарий PowerShell или Bash).</span><span class="sxs-lookup"><span data-stu-id="56f32-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f32-132">CommonParameters</span></span>
<span data-ttu-id="56f32-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f32-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56f32-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f32-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56f32-135">INPUTS</span></span>

### <span data-ttu-id="56f32-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="56f32-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="56f32-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56f32-137">OUTPUTS</span></span>

### <span data-ttu-id="56f32-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="56f32-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="56f32-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56f32-139">NOTES</span></span>

## <span data-ttu-id="56f32-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56f32-140">RELATED LINKS</span></span>

[<span data-ttu-id="56f32-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="56f32-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


