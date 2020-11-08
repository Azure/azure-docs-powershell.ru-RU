---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076476"
---
# <span data-ttu-id="c81cf-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c81cf-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="c81cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c81cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c81cf-103">Удаление кластера HDInsight из подписки.</span><span class="sxs-lookup"><span data-stu-id="c81cf-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="c81cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c81cf-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c81cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c81cf-105">DESCRIPTION</span></span>
<span data-ttu-id="c81cf-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="c81cf-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c81cf-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="c81cf-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c81cf-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c81cf-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c81cf-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c81cf-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c81cf-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="c81cf-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c81cf-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c81cf-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c81cf-112">Командлет **Remove-AzureHDInsightCluster** удаляет указанный кластер служб HDInsight из подписки.</span><span class="sxs-lookup"><span data-stu-id="c81cf-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="c81cf-113">Эта операция также удаляет все данные, хранящиеся в распределенной файловой системе Hadoop (HDFS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="c81cf-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="c81cf-114">Данные, хранящиеся в связанной учетной записи хранилища Azure, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="c81cf-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="c81cf-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c81cf-115">EXAMPLES</span></span>

### <span data-ttu-id="c81cf-116">Пример 1: Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="c81cf-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="c81cf-117">Эта команда удаляет кластер HDInsight с именем HDICluster.</span><span class="sxs-lookup"><span data-stu-id="c81cf-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="c81cf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c81cf-118">PARAMETERS</span></span>

### <span data-ttu-id="c81cf-119">-Certificate</span><span class="sxs-lookup"><span data-stu-id="c81cf-119">-Certificate</span></span>
<span data-ttu-id="c81cf-120">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c81cf-120">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81cf-121">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="c81cf-121">-Endpoint</span></span>
<span data-ttu-id="c81cf-122">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="c81cf-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="c81cf-123">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c81cf-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81cf-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="c81cf-124">-HostedService</span></span>
<span data-ttu-id="c81cf-125">Указывает пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c81cf-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81cf-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="c81cf-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="c81cf-127">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="c81cf-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81cf-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c81cf-128">-Name</span></span>
<span data-ttu-id="c81cf-129">Указывает имя кластера HDInsight для удаления.</span><span class="sxs-lookup"><span data-stu-id="c81cf-129">Specifies the name of the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81cf-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="c81cf-130">-Profile</span></span>
<span data-ttu-id="c81cf-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c81cf-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c81cf-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c81cf-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c81cf-133">-Подписка</span><span class="sxs-lookup"><span data-stu-id="c81cf-133">-Subscription</span></span>
<span data-ttu-id="c81cf-134">Указывает учетную запись подписки, которая содержит кластер HDInsight для удаления.</span><span class="sxs-lookup"><span data-stu-id="c81cf-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81cf-135">CommonParameters</span></span>
<span data-ttu-id="c81cf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c81cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81cf-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c81cf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81cf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c81cf-138">INPUTS</span></span>

## <span data-ttu-id="c81cf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c81cf-139">OUTPUTS</span></span>

## <span data-ttu-id="c81cf-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c81cf-140">NOTES</span></span>

## <span data-ttu-id="c81cf-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c81cf-141">RELATED LINKS</span></span>

[<span data-ttu-id="c81cf-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c81cf-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="c81cf-143">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c81cf-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="c81cf-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c81cf-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


