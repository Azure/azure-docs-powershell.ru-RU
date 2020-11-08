---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245391"
---
# <span data-ttu-id="4e02b-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="4e02b-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="4e02b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e02b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e02b-103">Добавляет настройку значения конфигурации Hadoop и (или) общей библиотеки куста в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="4e02b-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="4e02b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e02b-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e02b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e02b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e02b-106">Командлет **Add-AzHDInsightConfigValue** добавляет настройку значения конфигурации Hadoop, например core-site.xml или hive-site.xml и/или параметры общей библиотеки куста, для объекта конфигурации HDInsight, созданного с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4e02b-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4e02b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e02b-107">EXAMPLES</span></span>

### <span data-ttu-id="4e02b-108">Пример 1: Добавление настраиваемого значения конфигурации к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="4e02b-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="4e02b-109">Эта команда добавляет значение конфигурации Hadoop в кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="4e02b-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4e02b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e02b-110">PARAMETERS</span></span>

### <span data-ttu-id="4e02b-111">-Config</span><span class="sxs-lookup"><span data-stu-id="4e02b-111">-Config</span></span>
<span data-ttu-id="4e02b-112">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4e02b-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4e02b-113">Этот объект создается командлетом New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4e02b-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4e02b-114">-Core</span><span class="sxs-lookup"><span data-stu-id="4e02b-114">-Core</span></span>
<span data-ttu-id="4e02b-115">Задает основные конфигурации сайта для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e02b-116">-DefaultProfile</span></span>
<span data-ttu-id="4e02b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e02b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e02b-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="4e02b-118">-HBaseEnv</span></span>
<span data-ttu-id="4e02b-119">Задает конфигурации HBase в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="4e02b-120">-HBaseSite</span></span>
<span data-ttu-id="4e02b-121">Указывает конфигурации сайта HBase для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="4e02b-122">-Hdfs</span></span>
<span data-ttu-id="4e02b-123">Задает конфигурации HDFS для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="4e02b-124">-HiveEnv</span></span>
<span data-ttu-id="4e02b-125">Задает конфигурации куста для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="4e02b-126">-HiveSite</span></span>
<span data-ttu-id="4e02b-127">Задает конфигурации сайтов кустов в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="4e02b-128">-MapRed</span></span>
<span data-ttu-id="4e02b-129">Задает конфигурации сайта MapRed для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="4e02b-130">-OozieEnv</span></span>
<span data-ttu-id="4e02b-131">Задает конфигурации Oozie пер для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="4e02b-132">-OozieSite</span></span>
<span data-ttu-id="4e02b-133">Задает конфигурации сайта Oozie для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="4e02b-134">-RServer</span></span>
<span data-ttu-id="4e02b-135">Задает конфигурации RServer.</span><span class="sxs-lookup"><span data-stu-id="4e02b-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="4e02b-136">Действует только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="4e02b-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4e02b-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="4e02b-137">-Spark2Defaults</span></span>
<span data-ttu-id="4e02b-138">Задает конфигурации Spark2 по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="4e02b-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="4e02b-140">Указывает конфигурации Spark2 Thrift SparkConf для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="4e02b-141">-SparkDefaults</span></span>
<span data-ttu-id="4e02b-142">Задает конфигурации Spark по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="4e02b-143">-SparkThriftConf</span></span>
<span data-ttu-id="4e02b-144">Задает конфигурации Spark Thrift SparkConf в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-145">-Огонь</span><span class="sxs-lookup"><span data-stu-id="4e02b-145">-Storm</span></span>
<span data-ttu-id="4e02b-146">Задает конфигурации сайта с набором вариантов для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="4e02b-147">-Tez</span></span>
<span data-ttu-id="4e02b-148">Задает конфигурации сайта Tez для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="4e02b-149">-WebHCat</span></span>
<span data-ttu-id="4e02b-150">Задает конфигурации сайта WebHCat для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-151">-Yarn</span><span class="sxs-lookup"><span data-stu-id="4e02b-151">-Yarn</span></span>
<span data-ttu-id="4e02b-152">Задает конфигурации сайта YARN для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4e02b-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e02b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e02b-153">CommonParameters</span></span>
<span data-ttu-id="4e02b-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e02b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e02b-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e02b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e02b-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e02b-156">INPUTS</span></span>

### <span data-ttu-id="4e02b-157">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4e02b-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4e02b-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e02b-158">OUTPUTS</span></span>

### <span data-ttu-id="4e02b-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4e02b-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4e02b-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e02b-160">NOTES</span></span>

## <span data-ttu-id="4e02b-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e02b-161">RELATED LINKS</span></span>

[<span data-ttu-id="4e02b-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4e02b-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


