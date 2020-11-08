---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075923"
---
# <span data-ttu-id="2fe67-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fe67-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="2fe67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fe67-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe67-103">Создает кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="2fe67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fe67-104">SYNTAX</span></span>

### <span data-ttu-id="2fe67-105">Кластеризация по конфигурации (с определенными учетными данными подписки) (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fe67-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2fe67-106">Кластеризация по имени (с определенными учетными данными подписки)</span><span class="sxs-lookup"><span data-stu-id="2fe67-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2fe67-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fe67-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe67-108">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="2fe67-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="2fe67-109">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="2fe67-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="2fe67-110">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="2fe67-111">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="2fe67-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="2fe67-112">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="2fe67-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="2fe67-113">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2fe67-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="2fe67-114">Командлет **New-AzureHDInsightCluster** создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="2fe67-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="2fe67-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fe67-115">EXAMPLES</span></span>

### <span data-ttu-id="2fe67-116">Пример 1: Создание кластера HDInsight</span><span class="sxs-lookup"><span data-stu-id="2fe67-116">Example 1: Create an HDInsight cluster</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="2fe67-117">В этом примере создается кластер HDInsight для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="2fe67-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="2fe67-118">Первая команда использует командлет **Get-AzureSubscription** для получения текущего идентификатора подписки, а затем сохраняет его в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="2fe67-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="2fe67-119">Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохраняют ключи в переменных $Key 1 и $Key 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="2fe67-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="2fe67-120">Четвертые, пятого и шестые команды используют командлет **Get-Credential** для получения учетных данных для текущей подписки и для Oozie и Hive, а затем хранят учетные данные в переменных.</span><span class="sxs-lookup"><span data-stu-id="2fe67-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="2fe67-121">Последняя команда выполняет последовательность операций, используя следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="2fe67-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="2fe67-122">**New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="2fe67-123">**Set-AzureHDInsightDefaultStorage** , чтобы настроить учетную запись хранения по умолчанию для конфигурации MyBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="2fe67-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="2fe67-124">**Add-AzureHDInsightStorage** , чтобы добавить в конфигурацию вторую учетную запись хранения с именем MySecondBlobStorage.BLOB.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="2fe67-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="2fe67-125">**Add-AzureHDInsightMetastore** , чтобы добавить в конфигурацию MetaStore для Oozie и MetaStore для куста.</span><span class="sxs-lookup"><span data-stu-id="2fe67-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="2fe67-126">**New-AzureHDInsightCluster** , чтобы создать кластер HDInsight с новой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="2fe67-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="2fe67-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fe67-127">PARAMETERS</span></span>

### <span data-ttu-id="2fe67-128">-Certificate</span><span class="sxs-lookup"><span data-stu-id="2fe67-128">-Certificate</span></span>
<span data-ttu-id="2fe67-129">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe67-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="2fe67-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="2fe67-131">Задает количество узлов данных, которые нужно создать для кластера.</span><span class="sxs-lookup"><span data-stu-id="2fe67-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2fe67-132">-ClusterType</span></span>
<span data-ttu-id="2fe67-133">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="2fe67-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-134">-Config</span><span class="sxs-lookup"><span data-stu-id="2fe67-134">-Config</span></span>
<span data-ttu-id="2fe67-135">Указывает объект конфигурации, созданный с помощью командлета **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="2fe67-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="2fe67-136">-Credential</span></span>
<span data-ttu-id="2fe67-137">Указывает учетные данные пользователя для HDInsight, которые будут использоваться для учетной записи по умолчанию, используемой для удаленного доступа к кластеру Hadoop.</span><span class="sxs-lookup"><span data-stu-id="2fe67-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="2fe67-138">Эти учетные данные отличаются от учетных данных подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="2fe67-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="2fe67-139">-DataNodeVMSize</span></span>
<span data-ttu-id="2fe67-140">Задает размер виртуальной машины для узла данных.</span><span class="sxs-lookup"><span data-stu-id="2fe67-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fe67-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="2fe67-142">Указывает ключ учетной записи хранения, используемой по умолчанию, которую использует кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2fe67-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="2fe67-144">Указывает имя учетной записи хранения по умолчанию, используемой в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="2fe67-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="2fe67-146">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который используется кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-147">-EndPoint</span><span class="sxs-lookup"><span data-stu-id="2fe67-147">-EndPoint</span></span>
<span data-ttu-id="2fe67-148">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe67-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="2fe67-149">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2fe67-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="2fe67-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="2fe67-151">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="2fe67-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="2fe67-152">-HostedService</span></span>
<span data-ttu-id="2fe67-153">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="2fe67-154">Если этот параметр не указан, этот командлет использует пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2fe67-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="2fe67-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="2fe67-156">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="2fe67-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-157">-Location</span><span class="sxs-lookup"><span data-stu-id="2fe67-157">-Location</span></span>
<span data-ttu-id="2fe67-158">Указывает область, в которой нужно создать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fe67-159">-Name</span></span>
<span data-ttu-id="2fe67-160">Указывает имя создаваемого кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe67-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="2fe67-161">-OSType</span></span>
<span data-ttu-id="2fe67-162">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="2fe67-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-163">-Profile</span><span class="sxs-lookup"><span data-stu-id="2fe67-163">-Profile</span></span>
<span data-ttu-id="2fe67-164">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2fe67-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2fe67-165">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2fe67-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2fe67-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="2fe67-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="2fe67-167">Задает срок действия в виде объекта **DateTime** для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="2fe67-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="2fe67-168">-RdpCredential</span></span>
<span data-ttu-id="2fe67-169">Указывает учетные данные для доступа к кластеру по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="2fe67-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="2fe67-170">-SshCredential</span></span>
<span data-ttu-id="2fe67-171">Задает имя пользователя и пароль для кластера HDInsight с помощью Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="2fe67-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="2fe67-172">Этот параметр действует только для кластеров Linux.</span><span class="sxs-lookup"><span data-stu-id="2fe67-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2fe67-173">-SshPublicKey</span></span>
<span data-ttu-id="2fe67-174">Указывает открытый ключ SSH для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="2fe67-175">Этот параметр действует только для кластеров Linux.</span><span class="sxs-lookup"><span data-stu-id="2fe67-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="2fe67-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="2fe67-176">-SubnetName</span></span>
<span data-ttu-id="2fe67-177">Указывает имя подсети.</span><span class="sxs-lookup"><span data-stu-id="2fe67-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-178">-Подписка</span><span class="sxs-lookup"><span data-stu-id="2fe67-178">-Subscription</span></span>
<span data-ttu-id="2fe67-179">Указывает подписку на Azure, в которой нужно создать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fe67-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-180">-Version</span><span class="sxs-lookup"><span data-stu-id="2fe67-180">-Version</span></span>
<span data-ttu-id="2fe67-181">Определяет версию кластера HDInsight, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2fe67-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2fe67-182">-VirtualNetworkId</span></span>
<span data-ttu-id="2fe67-183">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="2fe67-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="2fe67-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="2fe67-185">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="2fe67-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="2fe67-186">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="2fe67-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe67-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe67-187">CommonParameters</span></span>
<span data-ttu-id="2fe67-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fe67-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe67-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe67-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe67-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fe67-190">INPUTS</span></span>

## <span data-ttu-id="2fe67-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fe67-191">OUTPUTS</span></span>

## <span data-ttu-id="2fe67-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fe67-192">NOTES</span></span>

## <span data-ttu-id="2fe67-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fe67-193">RELATED LINKS</span></span>

[<span data-ttu-id="2fe67-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="2fe67-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="2fe67-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="2fe67-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="2fe67-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fe67-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="2fe67-197">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2fe67-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="2fe67-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fe67-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="2fe67-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="2fe67-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="2fe67-200">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fe67-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


