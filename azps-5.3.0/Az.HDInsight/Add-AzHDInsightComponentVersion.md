---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: ae8d096da4a21b3f53efcd14fc28b19bd133b369
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507350"
---
# <span data-ttu-id="5357a-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="5357a-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="5357a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5357a-102">SYNOPSIS</span></span>
<span data-ttu-id="5357a-103">Добавляет версию службы, запущенной в кластере, в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="5357a-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="5357a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5357a-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5357a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5357a-105">DESCRIPTION</span></span>
<span data-ttu-id="5357a-106">Этот Add-AzHDInsightComponentVersion добавляет версию для службы, запущенной в кластере, к объекту конфигурации Azure HDInsight, созданному New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="5357a-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="5357a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5357a-107">EXAMPLES</span></span>

### <span data-ttu-id="5357a-108">Пример 1. Добавление версии спарка к объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="5357a-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="5357a-109">Эта команда добавляет версию спарка в кластер HDInsight с именем "ваш-спарк-001".</span><span class="sxs-lookup"><span data-stu-id="5357a-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="5357a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5357a-110">PARAMETERS</span></span>

### <span data-ttu-id="5357a-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="5357a-111">-ComponentName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5357a-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="5357a-112">-ComponentVersion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5357a-113">-Config</span><span class="sxs-lookup"><span data-stu-id="5357a-113">-Config</span></span>
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

### <span data-ttu-id="5357a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5357a-114">-DefaultProfile</span></span>
<span data-ttu-id="5357a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5357a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5357a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5357a-116">-Confirm</span></span>
<span data-ttu-id="5357a-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5357a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5357a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5357a-118">-WhatIf</span></span>
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

### <span data-ttu-id="5357a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5357a-119">CommonParameters</span></span>
<span data-ttu-id="5357a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5357a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5357a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5357a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5357a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5357a-122">INPUTS</span></span>

### <span data-ttu-id="5357a-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5357a-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5357a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5357a-124">OUTPUTS</span></span>

### <span data-ttu-id="5357a-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5357a-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5357a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5357a-126">NOTES</span></span>

## <span data-ttu-id="5357a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5357a-127">RELATED LINKS</span></span>
