---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075716"
---
# <span data-ttu-id="ee5f4-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ee5f4-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="ee5f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5f4-103">Добавляет запись учетной записи хранения BLOB в конфигурацию HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="ee5f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee5f4-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee5f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee5f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5f4-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ee5f4-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ee5f4-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ee5f4-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ee5f4-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ee5f4-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ee5f4-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ee5f4-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ee5f4-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ee5f4-112">Командлет **Add-AzureHDInsightStorage** добавляет запись учетной записи хранения BLOB в конфигурацию Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="ee5f4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee5f4-113">EXAMPLES</span></span>

### <span data-ttu-id="ee5f4-114">Пример 1: Добавление учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ee5f4-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="ee5f4-115">Эта команда добавляет учетную запись хранения с именем MyStorage в объект конфигурации, хранящийся в $Config, и сохраняет конфигурацию в переменной $StoreConfig.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="ee5f4-116">Пример 2: Настройка нескольких учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="ee5f4-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="ee5f4-117">Первая команда использует командлет **Get-AzureSubscription** для получения текущего идентификатора подписки, а затем сохраняет его в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="ee5f4-118">Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохраняют ключи в переменных $Key 1 и $Key 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="ee5f4-119">Четвертые, пятого и шестые команды получают учетные данные для текущей подписки и для Oozie и Hive, а затем хранят учетные данные в переменных.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="ee5f4-120">Последняя команда выполняет последовательность операций, используя следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="ee5f4-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="ee5f4-121">**New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight</span><span class="sxs-lookup"><span data-stu-id="ee5f4-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="ee5f4-122">**Set-AzureHDInsightDefaultStorage** , чтобы настроить учетную запись хранения по умолчанию для конфигурации MyBlobStorage.BLOB.Core.Windows.NET</span><span class="sxs-lookup"><span data-stu-id="ee5f4-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="ee5f4-123">**Add-AzureHDInsightStorage** , чтобы добавить в конфигурацию вторую учетную запись хранения с именем MySecondBlobStorage.BLOB.Core.Windows.NET</span><span class="sxs-lookup"><span data-stu-id="ee5f4-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="ee5f4-124">**Add-AzureHDInsightStorage** , чтобы добавить в конфигурацию MetaStore для Oozie и MetaStore для куста.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="ee5f4-125">**New-AzureHDInsightCluster** для создания кластера HDInsight с новой конфигурацией</span><span class="sxs-lookup"><span data-stu-id="ee5f4-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="ee5f4-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee5f4-126">PARAMETERS</span></span>

### <span data-ttu-id="ee5f4-127">-Config</span><span class="sxs-lookup"><span data-stu-id="ee5f4-127">-Config</span></span>
<span data-ttu-id="ee5f4-128">Указывает объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-128">Specifies a configuration object.</span></span>
<span data-ttu-id="ee5f4-129">Этот командлет добавляет данные учетной записи хранения в объект, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee5f4-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="ee5f4-130">-Profile</span></span>
<span data-ttu-id="ee5f4-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee5f4-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee5f4-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ee5f4-133">-StorageAccountKey</span></span>
<span data-ttu-id="ee5f4-134">Указывает ключ учетной записи хранения, который используется для доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="ee5f4-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ee5f4-135">-StorageAccountName</span></span>
<span data-ttu-id="ee5f4-136">Указывает имя учетной записи хранения Azure, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="ee5f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5f4-137">CommonParameters</span></span>
<span data-ttu-id="ee5f4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee5f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5f4-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5f4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5f4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee5f4-140">INPUTS</span></span>

## <span data-ttu-id="ee5f4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee5f4-141">OUTPUTS</span></span>

## <span data-ttu-id="ee5f4-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee5f4-142">NOTES</span></span>

## <span data-ttu-id="ee5f4-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee5f4-143">RELATED LINKS</span></span>

[<span data-ttu-id="ee5f4-144">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ee5f4-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="ee5f4-145">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ee5f4-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="ee5f4-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ee5f4-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


