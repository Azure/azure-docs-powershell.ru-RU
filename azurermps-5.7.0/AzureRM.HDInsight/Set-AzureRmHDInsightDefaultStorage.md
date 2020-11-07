---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: 43418937c379ba1ac93b5a2c733028e31eef7318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732860"
---
# <span data-ttu-id="eb7ea-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="eb7ea-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="eb7ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7ea-103">Задает параметр учетной записи хранения по умолчанию в объекте конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb7ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb7ea-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb7ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7ea-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7ea-106">Командлет **Set-AzureRmHDInsightDefaultStorage** задает параметры учетной записи хранения по умолчанию в объекте конфигурации кластера Azure HDInsight, созданном с помощью командлета New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="eb7ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb7ea-107">EXAMPLES</span></span>

### <span data-ttu-id="eb7ea-108">Пример 1: Настройка учетной записи хранения по умолчанию для объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="eb7ea-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="eb7ea-109">Эта команда задает учетную запись хранения по умолчанию для объекта конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="eb7ea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb7ea-110">PARAMETERS</span></span>

### <span data-ttu-id="eb7ea-111">-Config</span><span class="sxs-lookup"><span data-stu-id="eb7ea-111">-Config</span></span>
<span data-ttu-id="eb7ea-112">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="eb7ea-113">Этот объект создается командлетом **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="eb7ea-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7ea-114">-DefaultProfile</span></span>
<span data-ttu-id="eb7ea-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb7ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb7ea-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb7ea-116">-StorageAccountKey</span></span>
<span data-ttu-id="eb7ea-117">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ea-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eb7ea-118">-StorageAccountName</span></span>
<span data-ttu-id="eb7ea-119">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ea-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="eb7ea-120">-StorageAccountType</span></span>
<span data-ttu-id="eb7ea-121">Возвращает или задает тип учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="eb7ea-122">По умолчанию AzureStorage</span><span class="sxs-lookup"><span data-stu-id="eb7ea-122">Defaults to AzureStorage</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7ea-123">CommonParameters</span></span>
<span data-ttu-id="eb7ea-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7ea-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7ea-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb7ea-126">INPUTS</span></span>

### <span data-ttu-id="eb7ea-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="eb7ea-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="eb7ea-128">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb7ea-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="eb7ea-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7ea-129">OUTPUTS</span></span>

### <span data-ttu-id="eb7ea-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="eb7ea-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="eb7ea-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb7ea-131">NOTES</span></span>

## <span data-ttu-id="eb7ea-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb7ea-132">RELATED LINKS</span></span>

