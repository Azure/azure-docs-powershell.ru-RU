---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075728"
---
# <span data-ttu-id="46016-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="46016-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="46016-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46016-102">SYNOPSIS</span></span>
<span data-ttu-id="46016-103">Добавляет настройку значения конфигурации Hadoop или общей библиотеки куста в конфигурацию кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="46016-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="46016-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46016-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46016-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46016-105">DESCRIPTION</span></span>
<span data-ttu-id="46016-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="46016-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="46016-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="46016-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="46016-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="46016-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="46016-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="46016-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="46016-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="46016-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="46016-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="46016-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="46016-112">Командлет **Add-AzureHDInsightConfigValues** добавляет настройку значения конфигурации Hadoop, например Core-site.xml или Hive-site.xml или общую библиотеку куста для настройки кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="46016-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="46016-113">Командлет добавляет пользовательские значения конфигурации в указанный объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="46016-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="46016-114">Пользовательские параметры добавляются в файлы конфигурации для необходимых служб Hadoop при развертывании кластера.</span><span class="sxs-lookup"><span data-stu-id="46016-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="46016-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46016-115">EXAMPLES</span></span>

### <span data-ttu-id="46016-116">Пример 1: Настройка кластера</span><span class="sxs-lookup"><span data-stu-id="46016-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="46016-117">Первая команда создает новый объект **AzureHDInsightHiveConfiguration** , а затем сохраняет его в переменной $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="46016-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="46016-118">Следующие пять команд создают значения конфигурации Hive и хранят эти значения в качестве членов $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="46016-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="46016-119">С помощью седьмой команды создается объект **AzureHDInsightOozieConfiguration** , который затем сохраняется в переменной $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="46016-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="46016-120">Восьмая команда создает значение конфигурации для Oozie и сохраняет эти значения в качестве членов $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="46016-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="46016-121">Девятая команда создает объект **AzureHDInsightMapReduceConfiguration** и сохраняет его в переменной $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="46016-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="46016-122">Следующие две команды создают значения конфигурации MapReduce и хранят эти значения в качестве членов $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="46016-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="46016-123">Двенадцати команда использует командлет **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight и сохраняет его в переменной $config.</span><span class="sxs-lookup"><span data-stu-id="46016-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="46016-124">Команда использует оператор конвейера для передачи $Config командлету **Set-AzureHDInsightDefaultStorage** , чтобы обновить параметр хранения по умолчанию и командлет **Add-AzureHDInsightConfigValues** , чтобы добавить новые значения конфигурации в конфигурацию кластера.</span><span class="sxs-lookup"><span data-stu-id="46016-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="46016-125">Последняя команда использует оператор конвейера для передачи $Config командлету **New-AzureHDInsightCluster** для создания нового кластера HDInsight с настроенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="46016-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="46016-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46016-126">PARAMETERS</span></span>

### <span data-ttu-id="46016-127">-Config</span><span class="sxs-lookup"><span data-stu-id="46016-127">-Config</span></span>
<span data-ttu-id="46016-128">Указывает объект конфигурации, к которому нужно добавить конфигурацию Hadoop.</span><span class="sxs-lookup"><span data-stu-id="46016-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46016-129">-Core</span><span class="sxs-lookup"><span data-stu-id="46016-129">-Core</span></span>
<span data-ttu-id="46016-130">Задает набор значений конфигурации Hadoop для Core-site.xml.</span><span class="sxs-lookup"><span data-stu-id="46016-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="46016-131">-HBase</span></span>
<span data-ttu-id="46016-132">Задает набор значений конфигурации HBase для Hbase-site.xml.</span><span class="sxs-lookup"><span data-stu-id="46016-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-133">-HDFS</span><span class="sxs-lookup"><span data-stu-id="46016-133">-Hdfs</span></span>
<span data-ttu-id="46016-134">Задает набор значений конфигурации Hadoop для Hdfs-site.xml.</span><span class="sxs-lookup"><span data-stu-id="46016-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-135">-Куст</span><span class="sxs-lookup"><span data-stu-id="46016-135">-Hive</span></span>
<span data-ttu-id="46016-136">Задает объект настройки для службы Hive для Hadoop, включая набор значений конфигурации Hadoop для Hive-site.xml и кустов разделяемые библиотеки.</span><span class="sxs-lookup"><span data-stu-id="46016-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="46016-137">-MapReduce</span></span>
<span data-ttu-id="46016-138">Указывает объект настройки для MapReduce и планировщик мощностей.</span><span class="sxs-lookup"><span data-stu-id="46016-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="46016-139">-Oozie</span></span>
<span data-ttu-id="46016-140">Задает объект настройки для службы Hadoop Oozie, включая набор значений конфигурации Hadoop для Oozie-site.xml.</span><span class="sxs-lookup"><span data-stu-id="46016-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="46016-141">-Profile</span></span>
<span data-ttu-id="46016-142">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="46016-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46016-143">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46016-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46016-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="46016-144">-Spark</span></span>
<span data-ttu-id="46016-145">Указывает объект настройки для Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="46016-145">Specifies a customization object for Apache Spark.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-146">-Огонь</span><span class="sxs-lookup"><span data-stu-id="46016-146">-Storm</span></span>
<span data-ttu-id="46016-147">Указывает объект настройки для веб-обозревателя Apache.</span><span class="sxs-lookup"><span data-stu-id="46016-147">Specifies a customization object for Apache Storm.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-148">-Yarn</span><span class="sxs-lookup"><span data-stu-id="46016-148">-Yarn</span></span>
<span data-ttu-id="46016-149">Задает объект настройки для Hadoop YARN, задавая набор настраиваемых значений конфигурации YARN для Yarn-site.xml.</span><span class="sxs-lookup"><span data-stu-id="46016-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46016-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46016-150">CommonParameters</span></span>
<span data-ttu-id="46016-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46016-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46016-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46016-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46016-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46016-153">INPUTS</span></span>

## <span data-ttu-id="46016-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46016-154">OUTPUTS</span></span>

## <span data-ttu-id="46016-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="46016-155">NOTES</span></span>

## <span data-ttu-id="46016-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46016-156">RELATED LINKS</span></span>

[<span data-ttu-id="46016-157">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="46016-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="46016-158">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="46016-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="46016-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="46016-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
