---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075960"
---
# <span data-ttu-id="d356d-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="d356d-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="d356d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d356d-102">SYNOPSIS</span></span>
<span data-ttu-id="d356d-103">Задает учетную запись хранения по умолчанию для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d356d-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="d356d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d356d-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d356d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d356d-105">DESCRIPTION</span></span>
<span data-ttu-id="d356d-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="d356d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d356d-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="d356d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d356d-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d356d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d356d-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d356d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d356d-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d356d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d356d-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d356d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d356d-112">Командлет **Set-AzureHDInsightDefaultStorage** задает учетную запись хранения по умолчанию для конфигурации кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d356d-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="d356d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d356d-113">EXAMPLES</span></span>

### <span data-ttu-id="d356d-114">Пример 1: Настройка учетной записи хранения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d356d-114">Example 1: Set the default storage account</span></span>
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

<span data-ttu-id="d356d-115">Первая команда использует командлет **Get-AzureSubscription** для получения текущего идентификатора подписки, а затем сохраняет его в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="d356d-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="d356d-116">Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохраняют ключи в переменных $Key 1 и $Key 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="d356d-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="d356d-117">Четвертые, пятого и шестые команды используют командлет **Get-Credential** для получения учетных данных для текущей подписки, а затем хранят учетные данные в переменных $Creds, $OozieCreds и $HiveCreds.</span><span class="sxs-lookup"><span data-stu-id="d356d-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="d356d-118">Последняя команда выполняет последовательность операций, используя следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d356d-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="d356d-119">**New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d356d-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="d356d-120">**Set-AzureHDInsightDefaultStorage** , чтобы настроить учетную запись хранения по умолчанию для конфигурации MyBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="d356d-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="d356d-121">**Add-AzureHDInsightStorage** , чтобы добавить в конфигурацию вторую учетную запись хранения с именем MySecondBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="d356d-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="d356d-122">**Add-AzureHDInsightMetastore** , чтобы добавить в конфигурацию MetaStore для Oozie и MetaStore для куста.</span><span class="sxs-lookup"><span data-stu-id="d356d-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="d356d-123">**New-AzureHDInsightCluster** , чтобы создать кластер HDInsight с новой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="d356d-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="d356d-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d356d-124">PARAMETERS</span></span>

### <span data-ttu-id="d356d-125">-Config</span><span class="sxs-lookup"><span data-stu-id="d356d-125">-Config</span></span>
<span data-ttu-id="d356d-126">Указывает объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d356d-126">Specifies a configuration object.</span></span>
<span data-ttu-id="d356d-127">Этот командлет задает учетную запись хранения по умолчанию для объекта, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d356d-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="d356d-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="d356d-128">-Profile</span></span>
<span data-ttu-id="d356d-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d356d-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d356d-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d356d-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d356d-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d356d-131">-StorageAccountKey</span></span>
<span data-ttu-id="d356d-132">Указывает ключ учетной записи хранения, который используется для доступа к учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d356d-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="d356d-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d356d-133">-StorageAccountName</span></span>
<span data-ttu-id="d356d-134">Указывает имя учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d356d-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="d356d-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="d356d-135">-StorageContainerName</span></span>
<span data-ttu-id="d356d-136">Указывает имя контейнера хранилища по умолчанию для кластера.</span><span class="sxs-lookup"><span data-stu-id="d356d-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="d356d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d356d-137">CommonParameters</span></span>
<span data-ttu-id="d356d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d356d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d356d-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d356d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d356d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d356d-140">INPUTS</span></span>

## <span data-ttu-id="d356d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d356d-141">OUTPUTS</span></span>

## <span data-ttu-id="d356d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d356d-142">NOTES</span></span>

## <span data-ttu-id="d356d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d356d-143">RELATED LINKS</span></span>

[<span data-ttu-id="d356d-144">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="d356d-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="d356d-145">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="d356d-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="d356d-146">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d356d-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="d356d-147">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d356d-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


