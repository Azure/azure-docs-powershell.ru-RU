---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: e5d0e3b7ca23bb335e6b29f56feefefb07018e07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720856"
---
# <span data-ttu-id="323cf-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="323cf-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="323cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="323cf-102">SYNOPSIS</span></span>
<span data-ttu-id="323cf-103">Добавляет настройку значения конфигурации Hadoop и (или) общей библиотеки куста в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="323cf-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="323cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="323cf-104">SYNTAX</span></span>

### <span data-ttu-id="323cf-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="323cf-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="323cf-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="323cf-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="323cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="323cf-107">DESCRIPTION</span></span>
<span data-ttu-id="323cf-108">Командлет **Add-AzHDInsightConfigValue** добавляет настройку значения конфигурации Hadoop, например core-site.xml или hive-site.xml и/или параметры общей библиотеки куста, для объекта конфигурации HDInsight, созданного с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="323cf-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="323cf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="323cf-109">EXAMPLES</span></span>

### <span data-ttu-id="323cf-110">Пример 1: Добавление настраиваемого значения конфигурации к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="323cf-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="323cf-111">Эта команда добавляет значение конфигурации Hadoop в кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="323cf-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="323cf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="323cf-112">PARAMETERS</span></span>

### <span data-ttu-id="323cf-113">-Config</span><span class="sxs-lookup"><span data-stu-id="323cf-113">-Config</span></span>
<span data-ttu-id="323cf-114">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="323cf-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="323cf-115">Этот объект создается командлетом New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="323cf-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="323cf-116">-Core</span><span class="sxs-lookup"><span data-stu-id="323cf-116">-Core</span></span>
<span data-ttu-id="323cf-117">Задает основные конфигурации сайта для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323cf-118">-DefaultProfile</span></span>
<span data-ttu-id="323cf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="323cf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="323cf-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="323cf-120">-HBaseEnv</span></span>
<span data-ttu-id="323cf-121">Задает конфигурации HBase в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="323cf-122">-HBaseSite</span></span>
<span data-ttu-id="323cf-123">Указывает конфигурации сайта HBase для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="323cf-124">-Hdfs</span></span>
<span data-ttu-id="323cf-125">Задает конфигурации HDFS для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="323cf-126">-HiveEnv</span></span>
<span data-ttu-id="323cf-127">Задает конфигурации куста для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="323cf-128">-HiveSite</span></span>
<span data-ttu-id="323cf-129">Задает конфигурации сайтов кустов в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="323cf-130">-MapRed</span></span>
<span data-ttu-id="323cf-131">Задает конфигурации сайта MapRed для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="323cf-132">-OozieEnv</span></span>
<span data-ttu-id="323cf-133">Задает конфигурации Oozie пер для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="323cf-134">-OozieSite</span></span>
<span data-ttu-id="323cf-135">Задает конфигурации сайта Oozie для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="323cf-136">-RServer</span></span>
<span data-ttu-id="323cf-137">Задает конфигурации RServer.</span><span class="sxs-lookup"><span data-stu-id="323cf-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="323cf-138">Действует только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="323cf-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="323cf-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="323cf-139">-Spark2Defaults</span></span>
<span data-ttu-id="323cf-140">Задает конфигурации Spark2 по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323cf-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="323cf-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="323cf-142">Указывает конфигурации Spark2 Thrift SparkConf для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323cf-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="323cf-143">-SparkDefaults</span></span>
<span data-ttu-id="323cf-144">Задает конфигурации Spark по умолчанию для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323cf-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="323cf-145">-SparkThriftConf</span></span>
<span data-ttu-id="323cf-146">Задает конфигурации Spark Thrift SparkConf в этом кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323cf-147">-Огонь</span><span class="sxs-lookup"><span data-stu-id="323cf-147">-Storm</span></span>
<span data-ttu-id="323cf-148">Задает конфигурации сайта с набором вариантов для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="323cf-149">-Tez</span></span>
<span data-ttu-id="323cf-150">Задает конфигурации сайта Tez для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="323cf-151">-WebHCat</span></span>
<span data-ttu-id="323cf-152">Задает конфигурации сайта WebHCat для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="323cf-153">-Yarn</span></span>
<span data-ttu-id="323cf-154">Задает конфигурации сайта YARN для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="323cf-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="323cf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323cf-155">CommonParameters</span></span>
<span data-ttu-id="323cf-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="323cf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323cf-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="323cf-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323cf-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="323cf-158">INPUTS</span></span>

### <span data-ttu-id="323cf-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="323cf-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="323cf-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="323cf-160">OUTPUTS</span></span>

### <span data-ttu-id="323cf-161">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="323cf-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="323cf-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="323cf-162">NOTES</span></span>

## <span data-ttu-id="323cf-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="323cf-163">RELATED LINKS</span></span>

[<span data-ttu-id="323cf-164">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="323cf-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


