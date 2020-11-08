---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076434"
---
# <span data-ttu-id="43ae1-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43ae1-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="43ae1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="43ae1-103">Отключение доступа HTTP к кластеру.</span><span class="sxs-lookup"><span data-stu-id="43ae1-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="43ae1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43ae1-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43ae1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ae1-105">DESCRIPTION</span></span>
<span data-ttu-id="43ae1-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="43ae1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="43ae1-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="43ae1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="43ae1-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43ae1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="43ae1-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="43ae1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="43ae1-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="43ae1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="43ae1-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="43ae1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="43ae1-112">Командлет **REVOKE-AzureHDInsightHttpServicesAccess** отключает доступ HTTP к кластеру для веб-служб ODBC, Ambari, Oozie и WebHCatalog.</span><span class="sxs-lookup"><span data-stu-id="43ae1-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="43ae1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43ae1-113">EXAMPLES</span></span>

## <span data-ttu-id="43ae1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43ae1-114">PARAMETERS</span></span>

### <span data-ttu-id="43ae1-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="43ae1-115">-Certificate</span></span>
<span data-ttu-id="43ae1-116">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="43ae1-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="43ae1-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="43ae1-117">-Endpoint</span></span>
<span data-ttu-id="43ae1-118">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="43ae1-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="43ae1-119">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43ae1-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="43ae1-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="43ae1-120">-HostedService</span></span>
<span data-ttu-id="43ae1-121">Указывает пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43ae1-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="43ae1-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="43ae1-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="43ae1-123">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="43ae1-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="43ae1-124">-Location</span><span class="sxs-lookup"><span data-stu-id="43ae1-124">-Location</span></span>
<span data-ttu-id="43ae1-125">Указывает область, в которой находится кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43ae1-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ae1-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43ae1-126">-Name</span></span>
<span data-ttu-id="43ae1-127">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="43ae1-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="43ae1-128">Этот командлет отключает доступ по протоколу HTTP к кластеру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="43ae1-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="43ae1-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="43ae1-129">-Profile</span></span>
<span data-ttu-id="43ae1-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="43ae1-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43ae1-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43ae1-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43ae1-132">-Подписка</span><span class="sxs-lookup"><span data-stu-id="43ae1-132">-Subscription</span></span>
<span data-ttu-id="43ae1-133">Указывает учетную запись подписки, которая содержит кластер HDInsight для отзыва.</span><span class="sxs-lookup"><span data-stu-id="43ae1-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="43ae1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ae1-134">CommonParameters</span></span>
<span data-ttu-id="43ae1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43ae1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ae1-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ae1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ae1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43ae1-137">INPUTS</span></span>

## <span data-ttu-id="43ae1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ae1-138">OUTPUTS</span></span>

## <span data-ttu-id="43ae1-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="43ae1-139">NOTES</span></span>

## <span data-ttu-id="43ae1-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43ae1-140">RELATED LINKS</span></span>

[<span data-ttu-id="43ae1-141">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43ae1-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


