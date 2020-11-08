---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075723"
---
# <span data-ttu-id="89d02-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="89d02-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="89d02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89d02-102">SYNOPSIS</span></span>
<span data-ttu-id="89d02-103">Добавление учетной записи базы данных SQL Server в конфигурацию кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="89d02-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="89d02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89d02-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="89d02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89d02-105">DESCRIPTION</span></span>
<span data-ttu-id="89d02-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="89d02-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="89d02-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="89d02-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="89d02-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="89d02-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="89d02-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="89d02-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="89d02-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="89d02-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="89d02-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="89d02-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="89d02-112">Командлет **Add-AzureHDInsightMetastore** добавляет базу данных Microsoft SQL Server в конфигурацию HDInsight Azure, созданную с помощью командлета **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="89d02-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="89d02-113">База данных используется для хранения метаданных куста или Oozie или обоих типов.</span><span class="sxs-lookup"><span data-stu-id="89d02-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="89d02-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89d02-114">EXAMPLES</span></span>

### <span data-ttu-id="89d02-115">Пример 1: Добавление MetaStore</span><span class="sxs-lookup"><span data-stu-id="89d02-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="89d02-116">Эта команда добавляет базу данных SQL Server с именем ContosoSQLServer, которая будет использоваться в качестве куста MetaStore для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="89d02-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="89d02-117">Пример 2: Настройка хранилища и добавление metastores</span><span class="sxs-lookup"><span data-stu-id="89d02-117">Example 2: Configure storage and add metastores</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="89d02-118">Первая команда использует командлет **Get-AzureSubscription** для получения текущего идентификатора подписки, а затем сохраняет его в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="89d02-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="89d02-119">Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохраняют ключи в переменных $Key 1 и $Key 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="89d02-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="89d02-120">Четвертые, пятого и шестые команды используют командлет **Get-Credential** для получения учетных данных для текущей подписки и для Oozie и Hive, а затем хранят учетные данные в переменных.</span><span class="sxs-lookup"><span data-stu-id="89d02-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="89d02-121">Последняя команда выполняет последовательность операций, используя следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="89d02-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="89d02-122">**New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="89d02-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="89d02-123">**Set-AzureHDInsightDefaultStorage** , чтобы настроить учетную запись хранения по умолчанию для конфигурации MyBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="89d02-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="89d02-124">**Add-AzureHDInsightStorage** , чтобы добавить в конфигурацию вторую учетную запись хранения с именем MySecondBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="89d02-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="89d02-125">**Add-AzureHDInsightMetastore** , чтобы добавить в конфигурацию MetaStore для Oozie и MetaStore для куста.</span><span class="sxs-lookup"><span data-stu-id="89d02-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="89d02-126">**New-AzureHDInsightCluster** , чтобы создать кластер HDInsight с новой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="89d02-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="89d02-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89d02-127">PARAMETERS</span></span>

### <span data-ttu-id="89d02-128">-Config</span><span class="sxs-lookup"><span data-stu-id="89d02-128">-Config</span></span>
<span data-ttu-id="89d02-129">Указывает объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="89d02-129">Specifies a configuration object.</span></span>
<span data-ttu-id="89d02-130">Этот командлет добавляет данные MetaStore в объект конфигурации, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="89d02-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="89d02-131">-Credential</span><span class="sxs-lookup"><span data-stu-id="89d02-131">-Credential</span></span>
<span data-ttu-id="89d02-132">Указывает учетные данные, которые используются для доступа к базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="89d02-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d02-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89d02-133">-DatabaseName</span></span>
<span data-ttu-id="89d02-134">Указывает имя базы данных, в которой хранятся метаданные куста или Oozie.</span><span class="sxs-lookup"><span data-stu-id="89d02-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d02-135">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="89d02-135">-MetastoreType</span></span>
<span data-ttu-id="89d02-136">Указывает тип MetaStore.</span><span class="sxs-lookup"><span data-stu-id="89d02-136">Specifies the metastore type.</span></span>
<span data-ttu-id="89d02-137">Допустимые значения этого параметра: HiveMetaStore или OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="89d02-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d02-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="89d02-138">-Profile</span></span>
<span data-ttu-id="89d02-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89d02-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89d02-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89d02-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89d02-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="89d02-141">-SqlAzureServerName</span></span>
<span data-ttu-id="89d02-142">Указывает полное доменное имя (FQDN) сервера SQL Server, содержащего базу данных для хранения метаданных.</span><span class="sxs-lookup"><span data-stu-id="89d02-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d02-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d02-143">CommonParameters</span></span>
<span data-ttu-id="89d02-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89d02-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d02-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d02-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d02-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89d02-146">INPUTS</span></span>

## <span data-ttu-id="89d02-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89d02-147">OUTPUTS</span></span>

## <span data-ttu-id="89d02-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="89d02-148">NOTES</span></span>

## <span data-ttu-id="89d02-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89d02-149">RELATED LINKS</span></span>

[<span data-ttu-id="89d02-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="89d02-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="89d02-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="89d02-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="89d02-152">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="89d02-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="89d02-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="89d02-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
