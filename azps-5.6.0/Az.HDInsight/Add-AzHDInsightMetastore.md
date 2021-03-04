---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: 3b9f9b044a3009c1a1ba5bbc9789739237cb64c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990167"
---
# <span data-ttu-id="4fd07-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="4fd07-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="4fd07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd07-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd07-103">Добавляет в SQL кластера базу данных, которая будет служить метасемой "Оози" или "Оози".</span><span class="sxs-lookup"><span data-stu-id="4fd07-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="4fd07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fd07-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fd07-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd07-106">С помощью **cmdlet add-AzHDInsightMetastore** можно добавить метасхему "Гоголь" или "Oozie" в объект конфигурации HDInsight, созданный New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4fd07-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="4fd07-107">Метамагага — это база SQL, которая может хранить метаданные для оболя, оози или обоих этих метаданных.</span><span class="sxs-lookup"><span data-stu-id="4fd07-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="4fd07-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fd07-108">EXAMPLES</span></span>

### <span data-ttu-id="4fd07-109">Пример 1. Добавление метасхранилища SQL к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="4fd07-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="4fd07-110">Эта команда добавляет метас SQL базы данных в кластер с именем ваш-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="4fd07-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

### <span data-ttu-id="4fd07-111">Пример 2. Добавление настраиваемой базы данных Ambari к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="4fd07-111">Example 2: Add a custom Ambari database to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Custom Amari database info
PS C:\> $ambariSqlServer = "your-sqlserver-001"
PS C:\> $ambariDb = "your-sqldb-003"
PS C:\> $ambariCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$ambariSqlServer.database.contoso.net" `
                -DatabaseName $ambariDb `
                -Credential $ambariCreds `
                -MetastoreType AmbariDatabase `
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

<span data-ttu-id="4fd07-112">Эта команда добавляет настраиваемую базу данных Ambari в кластер с именем ваш-hadoop-002.</span><span class="sxs-lookup"><span data-stu-id="4fd07-112">This command adds a custom Ambari database to the cluster named your-hadoop-002.</span></span>

## <span data-ttu-id="4fd07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fd07-113">PARAMETERS</span></span>

### <span data-ttu-id="4fd07-114">-Config</span><span class="sxs-lookup"><span data-stu-id="4fd07-114">-Config</span></span>
<span data-ttu-id="4fd07-115">Определяет объект конфигурации кластера HDInsight, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd07-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4fd07-116">Этот объект создается с помощью **командылета New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="4fd07-116">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="4fd07-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="4fd07-117">-Credential</span></span>
<span data-ttu-id="4fd07-118">Определяет учетные данные для базы данных AzureSQL Server.</span><span class="sxs-lookup"><span data-stu-id="4fd07-118">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd07-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4fd07-119">-DatabaseName</span></span>
<span data-ttu-id="4fd07-120">Указывает базу данных в экземпляре AzureSQL Server, который будет использовать для этого метасхемы.</span><span class="sxs-lookup"><span data-stu-id="4fd07-120">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="4fd07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd07-121">-DefaultProfile</span></span>
<span data-ttu-id="4fd07-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4fd07-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fd07-123">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="4fd07-123">-MetastoreType</span></span>
<span data-ttu-id="4fd07-124">Тип метасхемы.</span><span class="sxs-lookup"><span data-stu-id="4fd07-124">Specifies the type of metastore.</span></span>
<span data-ttu-id="4fd07-125">Возможные значения: ОozieMetastore или ОozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="4fd07-125">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore, AmbariDatabase

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd07-126">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="4fd07-126">-SqlAzureServerName</span></span>
<span data-ttu-id="4fd07-127">Указывает экземпляр AzureSQL Server, который будет использовать для этого метасхемы.</span><span class="sxs-lookup"><span data-stu-id="4fd07-127">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="4fd07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd07-128">CommonParameters</span></span>
<span data-ttu-id="4fd07-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd07-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fd07-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd07-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fd07-131">INPUTS</span></span>

### <span data-ttu-id="4fd07-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4fd07-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4fd07-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fd07-133">OUTPUTS</span></span>

### <span data-ttu-id="4fd07-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4fd07-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4fd07-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fd07-135">NOTES</span></span>

## <span data-ttu-id="4fd07-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fd07-136">RELATED LINKS</span></span>

[<span data-ttu-id="4fd07-137">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4fd07-137">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


