---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 1f6a6d05bff2c012ca3b32abd16dca01cbe1707b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561803"
---
# <span data-ttu-id="bd45a-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bd45a-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="bd45a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd45a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd45a-103">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd45a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd45a-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd45a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd45a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd45a-106">Командлет **New-AzureRmHDInsightClusterConfig** создает несохраняемый объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="bd45a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd45a-107">EXAMPLES</span></span>

### <span data-ttu-id="bd45a-108">Пример 1: создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="bd45a-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
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

<span data-ttu-id="bd45a-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="bd45a-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="bd45a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd45a-110">PARAMETERS</span></span>

### <span data-ttu-id="bd45a-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="bd45a-111">-AadTenantId</span></span>
<span data-ttu-id="bd45a-112">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd45a-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="bd45a-113">-CertificateFileContents</span></span>
<span data-ttu-id="bd45a-114">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd45a-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="bd45a-115">-CertificateFilePath</span></span>
<span data-ttu-id="bd45a-116">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="bd45a-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="bd45a-117">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd45a-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="bd45a-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="bd45a-118">-CertificatePassword</span></span>
<span data-ttu-id="bd45a-119">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bd45a-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="bd45a-120">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd45a-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="bd45a-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="bd45a-121">-ClusterTier</span></span>
<span data-ttu-id="bd45a-122">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="bd45a-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bd45a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bd45a-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="bd45a-124">Standard</span></span>
- <span data-ttu-id="bd45a-125">Версию</span><span class="sxs-lookup"><span data-stu-id="bd45a-125">Premium</span></span>

<span data-ttu-id="bd45a-126">По умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="bd45a-126">The default value is Standard.</span></span>
<span data-ttu-id="bd45a-127">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="bd45a-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="bd45a-128">-ClusterType</span></span>
<span data-ttu-id="bd45a-129">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="bd45a-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="bd45a-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bd45a-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bd45a-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="bd45a-131">Hadoop</span></span>
- <span data-ttu-id="bd45a-132">HBase</span><span class="sxs-lookup"><span data-stu-id="bd45a-132">HBase</span></span>
- <span data-ttu-id="bd45a-133">Огонь</span><span class="sxs-lookup"><span data-stu-id="bd45a-133">Storm</span></span>
- <span data-ttu-id="bd45a-134">Spark</span><span class="sxs-lookup"><span data-stu-id="bd45a-134">Spark</span></span>

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

### <span data-ttu-id="bd45a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd45a-135">-DefaultProfile</span></span>
<span data-ttu-id="bd45a-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd45a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd45a-137">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd45a-137">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="bd45a-138">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-138">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="bd45a-139">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bd45a-139">-DefaultStorageAccountName</span></span>
<span data-ttu-id="bd45a-140">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-140">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="bd45a-141">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bd45a-141">-DefaultStorageAccountType</span></span>
<span data-ttu-id="bd45a-142">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-142">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="bd45a-143">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="bd45a-143">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-144">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="bd45a-144">-EdgeNodeSize</span></span>
<span data-ttu-id="bd45a-145">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="bd45a-145">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="bd45a-146">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-146">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="bd45a-147">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="bd45a-147">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="bd45a-148">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="bd45a-148">-HeadNodeSize</span></span>
<span data-ttu-id="bd45a-149">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="bd45a-149">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="bd45a-150">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-150">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="bd45a-151">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="bd45a-151">-HiveMetastore</span></span>
<span data-ttu-id="bd45a-152">Указывает MetaStore для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="bd45a-152">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="bd45a-153">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="bd45a-153">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-154">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bd45a-154">-ObjectId</span></span>
<span data-ttu-id="bd45a-155">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="bd45a-155">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="bd45a-156">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd45a-156">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-157">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="bd45a-157">-OozieMetastore</span></span>
<span data-ttu-id="bd45a-158">Указывает MetaStore для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="bd45a-158">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="bd45a-159">Вы также можете использовать командлет **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="bd45a-159">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd45a-160">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="bd45a-160">-WorkerNodeSize</span></span>
<span data-ttu-id="bd45a-161">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="bd45a-161">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="bd45a-162">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-162">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="bd45a-163">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="bd45a-163">-ZookeeperNodeSize</span></span>
<span data-ttu-id="bd45a-164">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="bd45a-164">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="bd45a-165">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd45a-165">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="bd45a-166">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="bd45a-166">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="bd45a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd45a-167">CommonParameters</span></span>
<span data-ttu-id="bd45a-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd45a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd45a-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd45a-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd45a-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd45a-170">INPUTS</span></span>

### <span data-ttu-id="bd45a-171">Ничего</span><span class="sxs-lookup"><span data-stu-id="bd45a-171">None</span></span>
<span data-ttu-id="bd45a-172">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bd45a-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd45a-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd45a-173">OUTPUTS</span></span>

### <span data-ttu-id="bd45a-174">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="bd45a-174">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="bd45a-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd45a-175">NOTES</span></span>

## <span data-ttu-id="bd45a-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd45a-176">RELATED LINKS</span></span>

[<span data-ttu-id="bd45a-177">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="bd45a-177">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


