---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: fcad97b2316e9db652fe4dc9df70bdc0f5d8b84d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074883"
---
# <span data-ttu-id="8aac4-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="8aac4-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="8aac4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8aac4-102">SYNOPSIS</span></span>
<span data-ttu-id="8aac4-103">Добавляет удостоверение кластера в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="8aac4-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="8aac4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8aac4-104">SYNTAX</span></span>

### <span data-ttu-id="8aac4-105">CertificateFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8aac4-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aac4-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8aac4-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aac4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aac4-107">DESCRIPTION</span></span>
<span data-ttu-id="8aac4-108">Командлет **Add-AzHDInsightClusterIdentity** добавляет удостоверение кластера в объект конфигурации HDInsight Azure, созданный командлетом New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="8aac4-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="8aac4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8aac4-109">EXAMPLES</span></span>

### <span data-ttu-id="8aac4-110">Пример 1: Добавление сведений об удостоверении кластера в объект конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="8aac4-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="8aac4-111">Эта команда добавляет сведения об удостоверении кластера в кластер с именем "-Hadoop-001", позволяя кластеру получить доступ к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8aac4-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="8aac4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8aac4-112">PARAMETERS</span></span>

### <span data-ttu-id="8aac4-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="8aac4-113">-AadTenantId</span></span>
<span data-ttu-id="8aac4-114">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8aac4-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aac4-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8aac4-115">-ApplicationId</span></span>
<span data-ttu-id="8aac4-116">Идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="8aac4-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="8aac4-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8aac4-117">-CertificateFileContents</span></span>
<span data-ttu-id="8aac4-118">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8aac4-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aac4-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8aac4-119">-CertificateFilePath</span></span>
<span data-ttu-id="8aac4-120">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="8aac4-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8aac4-121">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8aac4-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aac4-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8aac4-122">-CertificatePassword</span></span>
<span data-ttu-id="8aac4-123">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8aac4-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8aac4-124">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8aac4-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aac4-125">-Config</span><span class="sxs-lookup"><span data-stu-id="8aac4-125">-Config</span></span>
<span data-ttu-id="8aac4-126">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8aac4-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="8aac4-127">Этот объект создается командлетом New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="8aac4-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aac4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aac4-128">-DefaultProfile</span></span>
<span data-ttu-id="8aac4-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8aac4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aac4-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8aac4-130">-ObjectId</span></span>
<span data-ttu-id="8aac4-131">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="8aac4-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="8aac4-132">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8aac4-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aac4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aac4-133">CommonParameters</span></span>
<span data-ttu-id="8aac4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8aac4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aac4-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aac4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aac4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8aac4-136">INPUTS</span></span>

### <span data-ttu-id="8aac4-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8aac4-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="8aac4-138">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8aac4-138">System.Guid</span></span>

## <span data-ttu-id="8aac4-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aac4-139">OUTPUTS</span></span>

### <span data-ttu-id="8aac4-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8aac4-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8aac4-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8aac4-141">NOTES</span></span>

## <span data-ttu-id="8aac4-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8aac4-142">RELATED LINKS</span></span>

[<span data-ttu-id="8aac4-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8aac4-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


