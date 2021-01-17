---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322996"
---
# <span data-ttu-id="c0766-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c0766-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="c0766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0766-102">SYNOPSIS</span></span>
<span data-ttu-id="c0766-103">Создает объект конфигурации кластера, который не сохраняется и описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c0766-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0766-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0766-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0766-105">DESCRIPTION</span></span>
<span data-ttu-id="c0766-106">С **его** использованием создается объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c0766-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0766-107">EXAMPLES</span></span>

### <span data-ttu-id="c0766-108">Пример 1. Создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="c0766-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="c0766-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c0766-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="c0766-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0766-110">PARAMETERS</span></span>

### <span data-ttu-id="c0766-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c0766-111">-AadTenantId</span></span>
<span data-ttu-id="c0766-112">Определяет ИД клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0766-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c0766-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c0766-113">-ApplicationId</span></span>
<span data-ttu-id="c0766-114">Получает или задает ИД приложения-основной службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="c0766-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="c0766-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c0766-115">-AssignedIdentity</span></span>
<span data-ttu-id="c0766-116">Возвращает или устанавливает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="c0766-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="c0766-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c0766-117">-CertificateFileContents</span></span>
<span data-ttu-id="c0766-118">Определяет содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0766-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c0766-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c0766-119">-CertificateFilePath</span></span>
<span data-ttu-id="c0766-120">Путь к сертификату, который будет использоваться для проверки подлинности в качестве директора-службы.</span><span class="sxs-lookup"><span data-stu-id="c0766-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c0766-121">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0766-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c0766-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0766-122">-CertificatePassword</span></span>
<span data-ttu-id="c0766-123">Пароль сертификата, который будет использоваться для проверки подлинности в качестве директора-службы.</span><span class="sxs-lookup"><span data-stu-id="c0766-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c0766-124">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0766-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c0766-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c0766-125">-ClusterTier</span></span>
<span data-ttu-id="c0766-126">Определяет уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c0766-127">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c0766-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c0766-128">Стандартный</span><span class="sxs-lookup"><span data-stu-id="c0766-128">Standard</span></span>
- <span data-ttu-id="c0766-129">Premium Значение по умолчанию — "Стандартная".</span><span class="sxs-lookup"><span data-stu-id="c0766-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="c0766-130">Уровень Premium можно использовать только с кластерами Linux, и он позволяет использовать некоторые новые функции.</span><span class="sxs-lookup"><span data-stu-id="c0766-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c0766-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c0766-131">-ClusterType</span></span>
<span data-ttu-id="c0766-132">Тип кластера, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="c0766-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c0766-133">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c0766-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c0766-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="c0766-134">Hadoop</span></span>
- <span data-ttu-id="c0766-135">HBase</span><span class="sxs-lookup"><span data-stu-id="c0766-135">HBase</span></span>
- <span data-ttu-id="c0766-136">Ливн</span><span class="sxs-lookup"><span data-stu-id="c0766-136">Storm</span></span>
- <span data-ttu-id="c0766-137">Спарк</span><span class="sxs-lookup"><span data-stu-id="c0766-137">Spark</span></span>
- <span data-ttu-id="c0766-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="c0766-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="c0766-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="c0766-139">Kafka</span></span>
- <span data-ttu-id="c0766-140">RServer</span><span class="sxs-lookup"><span data-stu-id="c0766-140">RServer</span></span>

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

### <span data-ttu-id="c0766-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0766-141">-DefaultProfile</span></span>
<span data-ttu-id="c0766-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0766-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0766-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c0766-143">-EdgeNodeSize</span></span>
<span data-ttu-id="c0766-144">Определяет размер виртуальной машины для узла границы.</span><span class="sxs-lookup"><span data-stu-id="c0766-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c0766-145">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c0766-146">Этот параметр действителен только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="c0766-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c0766-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c0766-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="c0766-148">Получает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="c0766-148">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0766-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="c0766-149">-EncryptionAtHost</span></span>
<span data-ttu-id="c0766-150">Получает или устанавливает флажок, который указывает, следует ли включить шифрование на хосте.</span><span class="sxs-lookup"><span data-stu-id="c0766-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0766-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="c0766-151">-EncryptionInTransit</span></span>
<span data-ttu-id="c0766-152">Получает или устанавливает флажок, который указывает, следует ли включить шифрование при переходе.</span><span class="sxs-lookup"><span data-stu-id="c0766-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0766-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="c0766-153">-EncryptionKeyName</span></span>
<span data-ttu-id="c0766-154">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="c0766-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="c0766-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c0766-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="c0766-156">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="c0766-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="c0766-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="c0766-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="c0766-158">Получает или задает uri хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="c0766-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="c0766-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c0766-159">-HeadNodeSize</span></span>
<span data-ttu-id="c0766-160">Определяет размер виртуальной машины для узла head.</span><span class="sxs-lookup"><span data-stu-id="c0766-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c0766-161">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c0766-162">-Вельмеха</span><span class="sxs-lookup"><span data-stu-id="c0766-162">-HiveMetastore</span></span>
<span data-ttu-id="c0766-163">Указывает метасхранилище, в который будут храниться метаданные "Вирус".</span><span class="sxs-lookup"><span data-stu-id="c0766-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="c0766-164">Вы также можете использовать Add-AzHDInsightMetastore управления.</span><span class="sxs-lookup"><span data-stu-id="c0766-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c0766-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c0766-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="c0766-166">Получает или устанавливает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="c0766-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="c0766-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c0766-167">-ObjectId</span></span>
<span data-ttu-id="c0766-168">Определяет ИД объекта Azure AD (GUID) основного службы Azure AD, который представляет кластер.</span><span class="sxs-lookup"><span data-stu-id="c0766-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c0766-169">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0766-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c0766-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="c0766-170">-OozieMetastore</span></span>
<span data-ttu-id="c0766-171">Указывает метасхранилище для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="c0766-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="c0766-172">Вы также можете использовать для этого **cmdlet Add-AzHDInsightMetastore.**</span><span class="sxs-lookup"><span data-stu-id="c0766-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="c0766-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c0766-173">-StorageAccountKey</span></span>
<span data-ttu-id="c0766-174">Получает или задает ключ доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c0766-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="c0766-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c0766-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="c0766-176">Возвращает или устанавливает ид ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c0766-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="c0766-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c0766-177">-StorageAccountType</span></span>
<span data-ttu-id="c0766-178">Возвращает или задает тип учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0766-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0766-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c0766-179">-WorkerNodeSize</span></span>
<span data-ttu-id="c0766-180">Определяет размер виртуальной машины для узла "Работник".</span><span class="sxs-lookup"><span data-stu-id="c0766-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c0766-181">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c0766-182">-KeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c0766-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c0766-183">Определяет размер виртуальной машины для узлаKeeper.</span><span class="sxs-lookup"><span data-stu-id="c0766-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c0766-184">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c0766-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c0766-185">Этот параметр действителен только для кластеров HBase или Storm.</span><span class="sxs-lookup"><span data-stu-id="c0766-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c0766-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0766-186">CommonParameters</span></span>
<span data-ttu-id="c0766-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0766-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0766-188">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0766-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0766-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0766-189">INPUTS</span></span>

### <span data-ttu-id="c0766-190">Нет</span><span class="sxs-lookup"><span data-stu-id="c0766-190">None</span></span>

## <span data-ttu-id="c0766-191">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0766-191">OUTPUTS</span></span>

### <span data-ttu-id="c0766-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c0766-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c0766-193">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0766-193">NOTES</span></span>

## <span data-ttu-id="c0766-194">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0766-194">RELATED LINKS</span></span>

[<span data-ttu-id="c0766-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c0766-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


