---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 75d68b98d93168d69db4d5120dde41ca1a8f8f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563515"
---
# <span data-ttu-id="c293a-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="c293a-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="c293a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c293a-102">SYNOPSIS</span></span>
<span data-ttu-id="c293a-103">Добавляет настройку значения конфигурации Hadoop и (или) общей библиотеки куста в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c293a-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c293a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c293a-104">SYNTAX</span></span>

### <span data-ttu-id="c293a-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="c293a-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c293a-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="c293a-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c293a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c293a-107">DESCRIPTION</span></span>
<span data-ttu-id="c293a-108">Командлет **Add-AzureRmHDInsightConfigValues** добавляет настройку значения конфигурации Hadoop, например core-site.xml или hive-site.xml и/или параметры общей библиотеки куста, для объекта конфигурации HDInsight, созданного с помощью командлета New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c293a-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c293a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c293a-109">EXAMPLES</span></span>

### <span data-ttu-id="c293a-110">Пример 1: Добавление настраиваемого значения конфигурации к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="c293a-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="c293a-111">Эта команда добавляет значение конфигурации Hadoop в кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="c293a-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c293a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c293a-112">PARAMETERS</span></span>

### <span data-ttu-id="c293a-113">-Config</span><span class="sxs-lookup"><span data-stu-id="c293a-113">-Config</span></span>
<span data-ttu-id="c293a-114">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c293a-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c293a-115">Этот объект создается командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c293a-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="c293a-116">-Core</span><span class="sxs-lookup"><span data-stu-id="c293a-116">-Core</span></span>
<span data-ttu-id="c293a-117">Задает основные конфигурации сайта для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c293a-118">-DefaultProfile</span></span>
<span data-ttu-id="c293a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c293a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c293a-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="c293a-120">-HBaseEnv</span></span>
<span data-ttu-id="c293a-121">Задает конфигурации HBase в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="c293a-122">-HBaseSite</span></span>
<span data-ttu-id="c293a-123">Указывает конфигурации сайта HBase для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="c293a-124">-Hdfs</span></span>
<span data-ttu-id="c293a-125">Задает конфигурации HDFS для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="c293a-126">-HiveEnv</span></span>
<span data-ttu-id="c293a-127">Задает конфигурации куста для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="c293a-128">-HiveSite</span></span>
<span data-ttu-id="c293a-129">Задает конфигурации сайтов кустов в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="c293a-130">-MapRed</span></span>
<span data-ttu-id="c293a-131">Задает конфигурации сайта MapRed для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="c293a-132">-OozieEnv</span></span>
<span data-ttu-id="c293a-133">Задает конфигурации Oozie пер для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="c293a-134">-OozieSite</span></span>
<span data-ttu-id="c293a-135">Задает конфигурации сайта Oozie для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="c293a-136">-RServer</span></span>
<span data-ttu-id="c293a-137">Задает конфигурации RServer.</span><span class="sxs-lookup"><span data-stu-id="c293a-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="c293a-138">Действует только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="c293a-138">Valid only for RServer clusters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="c293a-139">-Spark2Defaults</span></span>
<span data-ttu-id="c293a-140">Задает конфигурации Spark2 по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="c293a-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="c293a-142">Указывает конфигурации Spark2 Thrift SparkConf для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="c293a-143">-SparkDefaults</span></span>
<span data-ttu-id="c293a-144">Задает конфигурации Spark по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="c293a-145">-SparkThriftConf</span></span>
<span data-ttu-id="c293a-146">Задает конфигурации Spark Thrift SparkConf в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-147">-Огонь</span><span class="sxs-lookup"><span data-stu-id="c293a-147">-Storm</span></span>
<span data-ttu-id="c293a-148">Задает конфигурации сайта с набором вариантов для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="c293a-149">-Tez</span></span>
<span data-ttu-id="c293a-150">Задает конфигурации сайта Tez для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="c293a-151">-WebHCat</span></span>
<span data-ttu-id="c293a-152">Задает конфигурации сайта WebHCat для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="c293a-153">-Yarn</span></span>
<span data-ttu-id="c293a-154">Задает конфигурации сайта YARN для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c293a-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c293a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c293a-155">CommonParameters</span></span>
<span data-ttu-id="c293a-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c293a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c293a-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c293a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c293a-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c293a-158">INPUTS</span></span>

### <span data-ttu-id="c293a-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c293a-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="c293a-160">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c293a-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="c293a-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c293a-161">OUTPUTS</span></span>

### <span data-ttu-id="c293a-162">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c293a-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c293a-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="c293a-163">NOTES</span></span>

## <span data-ttu-id="c293a-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c293a-164">RELATED LINKS</span></span>

[<span data-ttu-id="c293a-165">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c293a-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


