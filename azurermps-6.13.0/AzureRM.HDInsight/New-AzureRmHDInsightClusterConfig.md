---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: e4588f3799052cf9f397f846b635be4f525df930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564463"
---
# <span data-ttu-id="aeb4a-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="aeb4a-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="aeb4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aeb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb4a-103">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeb4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aeb4a-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeb4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeb4a-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb4a-106">Командлет **New-AzureRmHDInsightClusterConfig** создает несохраняемый объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="aeb4a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aeb4a-107">EXAMPLES</span></span>

### <span data-ttu-id="aeb4a-108">Пример 1: создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="aeb4a-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="aeb4a-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="aeb4a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aeb4a-110">PARAMETERS</span></span>

### <span data-ttu-id="aeb4a-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="aeb4a-111">-AadTenantId</span></span>
<span data-ttu-id="aeb4a-112">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="aeb4a-113">-CertificateFileContents</span></span>
<span data-ttu-id="aeb4a-114">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="aeb4a-115">-CertificateFilePath</span></span>
<span data-ttu-id="aeb4a-116">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="aeb4a-117">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="aeb4a-118">-CertificatePassword</span></span>
<span data-ttu-id="aeb4a-119">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="aeb4a-120">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="aeb4a-121">-ClusterTier</span></span>
<span data-ttu-id="aeb4a-122">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="aeb4a-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aeb4a-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aeb4a-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="aeb4a-124">Standard</span></span>
- <span data-ttu-id="aeb4a-125">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="aeb4a-126">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="aeb4a-127">-ClusterType</span></span>
<span data-ttu-id="aeb4a-128">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="aeb4a-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aeb4a-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aeb4a-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="aeb4a-130">Hadoop</span></span>
- <span data-ttu-id="aeb4a-131">HBase</span><span class="sxs-lookup"><span data-stu-id="aeb4a-131">HBase</span></span>
- <span data-ttu-id="aeb4a-132">Огонь</span><span class="sxs-lookup"><span data-stu-id="aeb4a-132">Storm</span></span>
- <span data-ttu-id="aeb4a-133">Spark</span><span class="sxs-lookup"><span data-stu-id="aeb4a-133">Spark</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb4a-134">-DefaultProfile</span></span>
<span data-ttu-id="aeb4a-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aeb4a-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aeb4a-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="aeb4a-137">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aeb4a-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="aeb4a-139">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aeb4a-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="aeb4a-141">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="aeb4a-142">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeb4a-143">-EdgeNodeSize</span></span>
<span data-ttu-id="aeb4a-144">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="aeb4a-145">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-145">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="aeb4a-146">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-146">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeb4a-147">-HeadNodeSize</span></span>
<span data-ttu-id="aeb4a-148">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="aeb4a-149">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-149">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="aeb4a-150">-HiveMetastore</span></span>
<span data-ttu-id="aeb4a-151">Указывает MetaStore для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="aeb4a-152">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-152">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aeb4a-153">-ObjectId</span></span>
<span data-ttu-id="aeb4a-154">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="aeb4a-155">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="aeb4a-156">-OozieMetastore</span></span>
<span data-ttu-id="aeb4a-157">Указывает MetaStore для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="aeb4a-158">Вы также можете использовать командлет **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="aeb4a-158">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeb4a-159">-WorkerNodeSize</span></span>
<span data-ttu-id="aeb4a-160">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="aeb4a-161">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-161">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeb4a-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="aeb4a-163">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="aeb4a-164">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-164">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="aeb4a-165">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-165">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb4a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb4a-166">CommonParameters</span></span>
<span data-ttu-id="aeb4a-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aeb4a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb4a-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb4a-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb4a-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aeb4a-169">INPUTS</span></span>

### <span data-ttu-id="aeb4a-170">Ничего</span><span class="sxs-lookup"><span data-stu-id="aeb4a-170">None</span></span>

## <span data-ttu-id="aeb4a-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeb4a-171">OUTPUTS</span></span>

### <span data-ttu-id="aeb4a-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="aeb4a-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="aeb4a-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="aeb4a-173">NOTES</span></span>

## <span data-ttu-id="aeb4a-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aeb4a-174">RELATED LINKS</span></span>

[<span data-ttu-id="aeb4a-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="aeb4a-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


