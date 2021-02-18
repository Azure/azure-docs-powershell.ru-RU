---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214673"
---
# <span data-ttu-id="04889-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="04889-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="04889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04889-102">SYNOPSIS</span></span>
<span data-ttu-id="04889-103">Добавляет настройку значения конфигурации Hadoop или общей библиотеки "Раздел" в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="04889-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="04889-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04889-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04889-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04889-105">DESCRIPTION</span></span>
<span data-ttu-id="04889-106">С помощью cmdlet **Add-AzHDInsightConfigValue** можно настроить значение конфигурации Hadoop, например core-site.xml или hive-site.xml, а также настроить общую библиотеку HDInsight в объект конфигурации HDInsight, созданный New-AzHDInsightClusterConfig-New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="04889-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="04889-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04889-107">EXAMPLES</span></span>

### <span data-ttu-id="04889-108">Пример 1. Добавление значения настраиваемой конфигурации к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="04889-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
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

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
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
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="04889-109">Эта команда добавляет значение конфигурации Hadoop в кластер с именем hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="04889-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="04889-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04889-110">PARAMETERS</span></span>

### <span data-ttu-id="04889-111">-Config</span><span class="sxs-lookup"><span data-stu-id="04889-111">-Config</span></span>
<span data-ttu-id="04889-112">Определяет объект конфигурации кластера HDInsight, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04889-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="04889-113">Этот объект создается с помощью New-AzHDInsightClusterConfig-управления.</span><span class="sxs-lookup"><span data-stu-id="04889-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="04889-114">-Core</span><span class="sxs-lookup"><span data-stu-id="04889-114">-Core</span></span>
<span data-ttu-id="04889-115">Определяет конфигурации основного сайта для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04889-116">-DefaultProfile</span></span>
<span data-ttu-id="04889-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="04889-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04889-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="04889-118">-HBaseEnv</span></span>
<span data-ttu-id="04889-119">Определяет конфигурации HBase Env для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="04889-120">-HBaseSite</span></span>
<span data-ttu-id="04889-121">Определяет конфигурации сайта HBase для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="04889-122">-Hdfs</span></span>
<span data-ttu-id="04889-123">Определяет конфигурации HDFS этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-124">-О-ваEnv</span><span class="sxs-lookup"><span data-stu-id="04889-124">-HiveEnv</span></span>
<span data-ttu-id="04889-125">Определяет конфигурацию этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-126">-Игогов</span><span class="sxs-lookup"><span data-stu-id="04889-126">-HiveSite</span></span>
<span data-ttu-id="04889-127">Определяет конфигурацию этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="04889-128">-MapRed</span></span>
<span data-ttu-id="04889-129">Определяет конфигурации сайта MapRed для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="04889-130">-OozieEnv</span></span>
<span data-ttu-id="04889-131">Определяет конфигурации Oozie Env для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="04889-132">-OozieSite</span></span>
<span data-ttu-id="04889-133">Определяет конфигурации сайта Oozie для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="04889-134">-RServer</span></span>
<span data-ttu-id="04889-135">Определяет конфигурации RServer.</span><span class="sxs-lookup"><span data-stu-id="04889-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="04889-136">Допустимо только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="04889-136">Valid only for RServer clusters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="04889-137">-Spark2Defaults</span></span>
<span data-ttu-id="04889-138">Определяет конфигурации по умолчанию для спарк2 для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="04889-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="04889-140">Определяет конфигурацию Спарк2 Tftft SparkConf для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="04889-141">-SparkDefaults</span></span>
<span data-ttu-id="04889-142">Определяет конфигурации по умолчанию спарк-по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="04889-143">-SparkThriftConf</span></span>
<span data-ttu-id="04889-144">Определяет конфигурацию спарк tft SparkConf для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="04889-145">-Storm</span></span>
<span data-ttu-id="04889-146">Определяет конфигурацию сайта storm для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="04889-147">-Tez</span></span>
<span data-ttu-id="04889-148">Определяет конфигурацию сайта Tez для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="04889-149">-WebHCat</span></span>
<span data-ttu-id="04889-150">Определяет конфигурацию сайта WebHCat для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-151">-Yarn</span><span class="sxs-lookup"><span data-stu-id="04889-151">-Yarn</span></span>
<span data-ttu-id="04889-152">Определяет конфигурации сайта YARN для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04889-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04889-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04889-153">CommonParameters</span></span>
<span data-ttu-id="04889-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04889-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04889-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04889-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04889-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04889-156">INPUTS</span></span>

### <span data-ttu-id="04889-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="04889-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="04889-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04889-158">OUTPUTS</span></span>

### <span data-ttu-id="04889-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="04889-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="04889-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04889-160">NOTES</span></span>

## <span data-ttu-id="04889-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04889-161">RELATED LINKS</span></span>

[<span data-ttu-id="04889-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="04889-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


