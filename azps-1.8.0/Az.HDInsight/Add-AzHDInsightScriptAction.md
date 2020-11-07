---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: b34fbf01196f5e25cb62ed7d9ecb0ba78aafa17f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900553"
---
# <span data-ttu-id="c27bb-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="c27bb-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="c27bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c27bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c27bb-103">Добавляет действие сценария в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c27bb-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="c27bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c27bb-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c27bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c27bb-105">DESCRIPTION</span></span>
<span data-ttu-id="c27bb-106">Командлет **Add-AzHDInsightScriptAction** добавляет действия сценария к объекту конфигурации HDInsight, созданному с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c27bb-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="c27bb-107">Действия с скриптами предоставляют функциональные возможности, которые используются для установки дополнительного программного обеспечения или для изменения конфигурации приложений, которые выполняются в кластере Hadoop, с помощью Windows PowerShell или сценариев bash (для кластеров Windows или Linux соответственно).</span><span class="sxs-lookup"><span data-stu-id="c27bb-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="c27bb-108">Действие сценария выполняется на узлах кластера при развертывании кластеров HDInsight и запускается после завершения настройки HDInsight узлами в кластере.</span><span class="sxs-lookup"><span data-stu-id="c27bb-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="c27bb-109">Действие сценария запускается с правами учетной записи системного администратора и предоставляет полные права на доступ к узлам кластера.</span><span class="sxs-lookup"><span data-stu-id="c27bb-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="c27bb-110">Вы можете предоставить каждому кластеру список действий сценария для выполнения в заданной последовательности.</span><span class="sxs-lookup"><span data-stu-id="c27bb-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="c27bb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c27bb-111">EXAMPLES</span></span>

### <span data-ttu-id="c27bb-112">Пример 1: Добавление действия сценария в объект конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="c27bb-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="c27bb-113">Эта команда добавляет действие сценария для узлов Head и Worker в кластере "-Hadoop-001", которое будет выполняться при завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="c27bb-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="c27bb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c27bb-114">PARAMETERS</span></span>

### <span data-ttu-id="c27bb-115">-Config</span><span class="sxs-lookup"><span data-stu-id="c27bb-115">-Config</span></span>
<span data-ttu-id="c27bb-116">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c27bb-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c27bb-117">Этот объект создается командлетом **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="c27bb-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="c27bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27bb-118">-DefaultProfile</span></span>
<span data-ttu-id="c27bb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c27bb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c27bb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c27bb-120">-Name</span></span>
<span data-ttu-id="c27bb-121">Задает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="c27bb-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="c27bb-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c27bb-122">-NodeType</span></span>
<span data-ttu-id="c27bb-123">Указывает тип узла, на котором будет выполняться действие сценария.</span><span class="sxs-lookup"><span data-stu-id="c27bb-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="c27bb-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c27bb-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c27bb-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="c27bb-125">HeadNode</span></span>
- <span data-ttu-id="c27bb-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="c27bb-126">WorkerNode</span></span>
- <span data-ttu-id="c27bb-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="c27bb-127">ZookeeperNode</span></span>

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

### <span data-ttu-id="c27bb-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="c27bb-128">-Parameters</span></span>
<span data-ttu-id="c27bb-129">Задает параметры действия сценария.</span><span class="sxs-lookup"><span data-stu-id="c27bb-129">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="c27bb-130">-URI</span><span class="sxs-lookup"><span data-stu-id="c27bb-130">-Uri</span></span>
<span data-ttu-id="c27bb-131">Задает общедоступный URI для действия сценария (сценарий PowerShell или bash).</span><span class="sxs-lookup"><span data-stu-id="c27bb-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="c27bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27bb-132">CommonParameters</span></span>
<span data-ttu-id="c27bb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c27bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27bb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c27bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27bb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c27bb-135">INPUTS</span></span>

### <span data-ttu-id="c27bb-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c27bb-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c27bb-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c27bb-137">OUTPUTS</span></span>

### <span data-ttu-id="c27bb-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c27bb-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c27bb-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c27bb-139">NOTES</span></span>

## <span data-ttu-id="c27bb-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c27bb-140">RELATED LINKS</span></span>

[<span data-ttu-id="c27bb-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c27bb-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


