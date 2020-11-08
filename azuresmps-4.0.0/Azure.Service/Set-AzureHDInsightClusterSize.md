---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075962"
---
# <span data-ttu-id="56cdc-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="56cdc-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="56cdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="56cdc-103">Задает количество узлов данных для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="56cdc-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="56cdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56cdc-104">SYNTAX</span></span>

### <span data-ttu-id="56cdc-105">Укажите размер кластера в узлах с именем.</span><span class="sxs-lookup"><span data-stu-id="56cdc-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="56cdc-106">Установка размера кластера в узлах с кластером из конвейера.</span><span class="sxs-lookup"><span data-stu-id="56cdc-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="56cdc-107">Кластеризация по имени (с определенными учетными данными подписки)</span><span class="sxs-lookup"><span data-stu-id="56cdc-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56cdc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="56cdc-109">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="56cdc-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="56cdc-110">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="56cdc-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="56cdc-111">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="56cdc-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="56cdc-112">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="56cdc-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="56cdc-113">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="56cdc-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="56cdc-114">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="56cdc-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="56cdc-115">Командлет **Set-AzureHDInsightClusterSize** задает количество узлов данных для кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="56cdc-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="56cdc-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56cdc-116">EXAMPLES</span></span>

## <span data-ttu-id="56cdc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56cdc-117">PARAMETERS</span></span>

### <span data-ttu-id="56cdc-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="56cdc-118">-Certificate</span></span>
<span data-ttu-id="56cdc-119">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="56cdc-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-120">-Cluster</span><span class="sxs-lookup"><span data-stu-id="56cdc-120">-Cluster</span></span>
<span data-ttu-id="56cdc-121">Задает кластер, размер которого нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="56cdc-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="56cdc-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="56cdc-123">Задает количество узлов данных, которые нужно создать для кластера.</span><span class="sxs-lookup"><span data-stu-id="56cdc-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="56cdc-124">-Endpoint</span></span>
<span data-ttu-id="56cdc-125">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="56cdc-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="56cdc-126">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56cdc-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-127">-Force</span><span class="sxs-lookup"><span data-stu-id="56cdc-127">-Force</span></span>
<span data-ttu-id="56cdc-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="56cdc-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="56cdc-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="56cdc-130">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="56cdc-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56cdc-131">-Name</span></span>
<span data-ttu-id="56cdc-132">Указывает имя кластера HDInsight, для которого нужно изменить размер.</span><span class="sxs-lookup"><span data-stu-id="56cdc-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="56cdc-133">-Profile</span></span>
<span data-ttu-id="56cdc-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="56cdc-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56cdc-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56cdc-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-136">-Подписка</span><span class="sxs-lookup"><span data-stu-id="56cdc-136">-Subscription</span></span>
<span data-ttu-id="56cdc-137">Указывает подписку.</span><span class="sxs-lookup"><span data-stu-id="56cdc-137">Specifies a subscription.</span></span>
<span data-ttu-id="56cdc-138">Этот командлет задает размер кластера для подписки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="56cdc-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cdc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cdc-139">CommonParameters</span></span>
<span data-ttu-id="56cdc-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56cdc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cdc-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56cdc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cdc-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56cdc-142">INPUTS</span></span>

## <span data-ttu-id="56cdc-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56cdc-143">OUTPUTS</span></span>

## <span data-ttu-id="56cdc-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="56cdc-144">NOTES</span></span>

## <span data-ttu-id="56cdc-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56cdc-145">RELATED LINKS</span></span>

