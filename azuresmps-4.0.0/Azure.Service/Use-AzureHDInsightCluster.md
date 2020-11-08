---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075837"
---
# <span data-ttu-id="0a96a-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0a96a-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="0a96a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a96a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a96a-103">Выбирает кластер HDInsight для командлета Invoke-AzureHDInsightHiveJob, который будет использоваться для отправки заданий.</span><span class="sxs-lookup"><span data-stu-id="0a96a-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="0a96a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a96a-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a96a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a96a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a96a-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="0a96a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="0a96a-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="0a96a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="0a96a-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0a96a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="0a96a-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="0a96a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="0a96a-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="0a96a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="0a96a-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0a96a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="0a96a-112">Командлет **use-AzureHDInsightCluster** выбирает кластер Azure HDInsight для командлета **Invoke-AzureHDInsightHiveJob** , который будет использоваться для отправки заданий.</span><span class="sxs-lookup"><span data-stu-id="0a96a-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="0a96a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a96a-113">EXAMPLES</span></span>

## <span data-ttu-id="0a96a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a96a-114">PARAMETERS</span></span>

### <span data-ttu-id="0a96a-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="0a96a-115">-Certificate</span></span>
<span data-ttu-id="0a96a-116">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="0a96a-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="0a96a-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="0a96a-117">-Endpoint</span></span>
<span data-ttu-id="0a96a-118">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="0a96a-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="0a96a-119">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a96a-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="0a96a-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="0a96a-120">-HostedService</span></span>
<span data-ttu-id="0a96a-121">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0a96a-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="0a96a-122">Если этот параметр не указан, используется пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a96a-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="0a96a-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="0a96a-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="0a96a-124">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="0a96a-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="0a96a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a96a-125">-Name</span></span>
<span data-ttu-id="0a96a-126">Указывает имя кластера, используемого командлетом **Invoke-AzureHDInsightHiveJob** .</span><span class="sxs-lookup"><span data-stu-id="0a96a-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="0a96a-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a96a-127">-Profile</span></span>
<span data-ttu-id="0a96a-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0a96a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a96a-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a96a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a96a-130">-Подписка</span><span class="sxs-lookup"><span data-stu-id="0a96a-130">-Subscription</span></span>
<span data-ttu-id="0a96a-131">Указывает подписку, которая содержит используемые кластеры HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0a96a-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="0a96a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a96a-132">CommonParameters</span></span>
<span data-ttu-id="0a96a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a96a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a96a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a96a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a96a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a96a-135">INPUTS</span></span>

## <span data-ttu-id="0a96a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a96a-136">OUTPUTS</span></span>

## <span data-ttu-id="0a96a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a96a-137">NOTES</span></span>

## <span data-ttu-id="0a96a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a96a-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a96a-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0a96a-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="0a96a-140">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0a96a-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="0a96a-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0a96a-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


