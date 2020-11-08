---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075920"
---
# <span data-ttu-id="60b09-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="60b09-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="60b09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60b09-102">SYNOPSIS</span></span>
<span data-ttu-id="60b09-103">Создание конфигурации нематериализованных кластеров HDInsight.</span><span class="sxs-lookup"><span data-stu-id="60b09-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="60b09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60b09-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="60b09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60b09-105">DESCRIPTION</span></span>
<span data-ttu-id="60b09-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="60b09-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="60b09-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="60b09-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="60b09-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="60b09-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="60b09-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="60b09-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="60b09-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="60b09-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="60b09-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="60b09-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="60b09-112">Командлет **New-AzureHDInsightClusterConfig** создает несохраняемую конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="60b09-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="60b09-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60b09-113">EXAMPLES</span></span>

### <span data-ttu-id="60b09-114">Пример 1: создание конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="60b09-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="60b09-115">Первая команда использует командлет **Get-AzureSubscription** для получения текущего идентификатора подписки, а затем сохраняет его в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="60b09-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="60b09-116">Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохраняют ключи в переменных $Key 1 и $Key 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="60b09-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="60b09-117">Четвертые, пятого и шестые команды используют командлет **Get-Credential** для получения учетных данных для текущей подписки и для Oozie и Hive, а затем хранят учетные данные в переменных.</span><span class="sxs-lookup"><span data-stu-id="60b09-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="60b09-118">Последняя команда выполняет последовательность операций, используя следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="60b09-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="60b09-119">**New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="60b09-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="60b09-120">**Set-AzureHDInsightDefaultStorage** , чтобы настроить учетную запись хранения по умолчанию для конфигурации MyBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="60b09-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="60b09-121">**Add-AzureHDInsightStorage** , чтобы добавить в конфигурацию вторую учетную запись хранения с именем MySecondBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="60b09-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="60b09-122">**Add-AzureHDInsightMetastore** , чтобы добавить в конфигурацию MetaStore для Oozie и MetaStore для куста.</span><span class="sxs-lookup"><span data-stu-id="60b09-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="60b09-123">**New-AzureHDInsightCluster** , чтобы создать кластер HDInsight с новой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="60b09-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="60b09-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60b09-124">PARAMETERS</span></span>

### <span data-ttu-id="60b09-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="60b09-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="60b09-126">Задает количество узлов данных, которые нужно создать для кластера.</span><span class="sxs-lookup"><span data-stu-id="60b09-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="60b09-127">-ClusterType</span></span>
<span data-ttu-id="60b09-128">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="60b09-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="60b09-129">-DataNodeVMSize</span></span>
<span data-ttu-id="60b09-130">Задает размер виртуальной машины для узла данных.</span><span class="sxs-lookup"><span data-stu-id="60b09-130">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="60b09-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="60b09-132">Задает размер виртуальной машины головного узла для кластера.</span><span class="sxs-lookup"><span data-stu-id="60b09-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="60b09-133">-Profile</span></span>
<span data-ttu-id="60b09-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="60b09-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60b09-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60b09-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="60b09-136">-SubnetName</span></span>
<span data-ttu-id="60b09-137">Указывает имя подсети.</span><span class="sxs-lookup"><span data-stu-id="60b09-137">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="60b09-138">-VirtualNetworkId</span></span>
<span data-ttu-id="60b09-139">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="60b09-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="60b09-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="60b09-141">Указывает размер виртуальной машины для узла Джесс в кластере HBase или в наборе.</span><span class="sxs-lookup"><span data-stu-id="60b09-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b09-142">CommonParameters</span></span>
<span data-ttu-id="60b09-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60b09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b09-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b09-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b09-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60b09-145">INPUTS</span></span>

## <span data-ttu-id="60b09-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60b09-146">OUTPUTS</span></span>

## <span data-ttu-id="60b09-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="60b09-147">NOTES</span></span>

## <span data-ttu-id="60b09-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60b09-148">RELATED LINKS</span></span>

[<span data-ttu-id="60b09-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="60b09-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="60b09-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="60b09-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="60b09-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="60b09-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="60b09-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="60b09-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


