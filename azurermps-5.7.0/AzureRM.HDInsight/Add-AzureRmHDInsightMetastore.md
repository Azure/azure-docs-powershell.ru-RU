---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: bc9b5a05111fff64b41400093d1f9c1ba3c2df8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563516"
---
# <span data-ttu-id="cb7b3-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="cb7b3-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="cb7b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7b3-103">Добавляет базу данных SQL, которая будет служить кустом или Oozie MetaStore объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb7b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb7b3-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb7b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb7b3-106">Командлет **Add-AzureRmHDInsightMetastore** добавляет куст или Oozie MetaStore в объект конфигурации HDInsight, созданный командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="cb7b3-107">MetaStore — это база данных SQL, которая может использоваться для хранения метаданных для куста, Oozie или и того, и для того и для других.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="cb7b3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb7b3-108">EXAMPLES</span></span>

### <span data-ttu-id="cb7b3-109">Пример 1: Добавление базы данных SQL MetaStore к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="cb7b3-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="cb7b3-110">Эта команда добавляет базу данных SQL MetaStore в кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="cb7b3-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="cb7b3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb7b3-111">PARAMETERS</span></span>

### <span data-ttu-id="cb7b3-112">-Config</span><span class="sxs-lookup"><span data-stu-id="cb7b3-112">-Config</span></span>
<span data-ttu-id="cb7b3-113">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="cb7b3-114">Этот объект создается командлетом **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="cb7b3-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b3-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="cb7b3-115">-Credential</span></span>
<span data-ttu-id="cb7b3-116">Указывает учетные данные, которые следует использовать для базы данных сервера AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb7b3-117">-DatabaseName</span></span>
<span data-ttu-id="cb7b3-118">Определяет базу данных на экземпляре сервера AzureSQL, который будет использоваться для этого MetaStore.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7b3-119">-DefaultProfile</span></span>
<span data-ttu-id="cb7b3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cb7b3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b3-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="cb7b3-121">-MetastoreType</span></span>
<span data-ttu-id="cb7b3-122">Указывает тип MetaStore.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="cb7b3-123">Возможные значения: HiveMetastore или OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b3-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="cb7b3-124">-SqlAzureServerName</span></span>
<span data-ttu-id="cb7b3-125">Указывает экземпляр сервера AzureSQL, который будет использоваться для этого MetaStore.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7b3-126">CommonParameters</span></span>
<span data-ttu-id="cb7b3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7b3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7b3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb7b3-129">INPUTS</span></span>

### <span data-ttu-id="cb7b3-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b3-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="cb7b3-131">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="cb7b3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb7b3-132">OUTPUTS</span></span>

### <span data-ttu-id="cb7b3-133">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b3-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cb7b3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb7b3-134">NOTES</span></span>

## <span data-ttu-id="cb7b3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb7b3-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb7b3-136">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b3-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


