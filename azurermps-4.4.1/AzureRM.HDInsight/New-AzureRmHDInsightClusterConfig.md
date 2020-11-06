---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569444"
---
# <span data-ttu-id="de648-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="de648-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="de648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de648-102">SYNOPSIS</span></span>
<span data-ttu-id="de648-103">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de648-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de648-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de648-105">DESCRIPTION</span></span>
<span data-ttu-id="de648-106">Командлет **New-AzureRmHDInsightClusterConfig** создает несохраняемый объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="de648-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de648-107">EXAMPLES</span></span>

### <span data-ttu-id="de648-108">Пример 1: создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="de648-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="de648-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="de648-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="de648-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de648-110">PARAMETERS</span></span>

### <span data-ttu-id="de648-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="de648-111">-AadTenantId</span></span>
<span data-ttu-id="de648-112">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de648-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="de648-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="de648-113">-CertificateFileContents</span></span>
<span data-ttu-id="de648-114">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de648-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="de648-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="de648-115">-CertificateFilePath</span></span>
<span data-ttu-id="de648-116">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="de648-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="de648-117">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de648-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="de648-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="de648-118">-CertificatePassword</span></span>
<span data-ttu-id="de648-119">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="de648-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="de648-120">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de648-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="de648-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="de648-121">-ClusterTier</span></span>
<span data-ttu-id="de648-122">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="de648-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="de648-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de648-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="de648-124">Standard</span></span>
- <span data-ttu-id="de648-125">Версию</span><span class="sxs-lookup"><span data-stu-id="de648-125">Premium</span></span>

<span data-ttu-id="de648-126">По умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="de648-126">The default value is Standard.</span></span>
<span data-ttu-id="de648-127">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="de648-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="de648-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="de648-128">-ClusterType</span></span>
<span data-ttu-id="de648-129">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="de648-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="de648-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="de648-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de648-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="de648-131">Hadoop</span></span>
- <span data-ttu-id="de648-132">HBase</span><span class="sxs-lookup"><span data-stu-id="de648-132">HBase</span></span>
- <span data-ttu-id="de648-133">Огонь</span><span class="sxs-lookup"><span data-stu-id="de648-133">Storm</span></span>
- <span data-ttu-id="de648-134">Spark</span><span class="sxs-lookup"><span data-stu-id="de648-134">Spark</span></span>

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

### <span data-ttu-id="de648-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="de648-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="de648-136">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="de648-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="de648-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="de648-138">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="de648-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="de648-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="de648-140">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="de648-141">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="de648-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="de648-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="de648-142">-EdgeNodeSize</span></span>
<span data-ttu-id="de648-143">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="de648-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="de648-144">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="de648-145">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="de648-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="de648-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="de648-146">-HeadNodeSize</span></span>
<span data-ttu-id="de648-147">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="de648-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="de648-148">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="de648-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="de648-149">-HiveMetastore</span></span>
<span data-ttu-id="de648-150">Указывает MetaStore для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="de648-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="de648-151">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="de648-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="de648-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="de648-152">-ObjectId</span></span>
<span data-ttu-id="de648-153">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="de648-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="de648-154">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de648-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="de648-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="de648-155">-OozieMetastore</span></span>
<span data-ttu-id="de648-156">Указывает MetaStore для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="de648-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="de648-157">Вы также можете использовать командлет **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="de648-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="de648-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="de648-158">-WorkerNodeSize</span></span>
<span data-ttu-id="de648-159">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="de648-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="de648-160">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="de648-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="de648-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="de648-162">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="de648-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="de648-163">Используйте Get-AzureRMVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de648-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="de648-164">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="de648-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="de648-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de648-165">-DefaultProfile</span></span>
<span data-ttu-id="de648-166">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de648-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de648-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de648-167">CommonParameters</span></span>
<span data-ttu-id="de648-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de648-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de648-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de648-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de648-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de648-170">INPUTS</span></span>

## <span data-ttu-id="de648-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de648-171">OUTPUTS</span></span>

### <span data-ttu-id="de648-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="de648-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="de648-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="de648-173">NOTES</span></span>

## <span data-ttu-id="de648-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de648-174">RELATED LINKS</span></span>

[<span data-ttu-id="de648-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="de648-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


