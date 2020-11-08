---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075764"
---
# <span data-ttu-id="b3ab1-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b3ab1-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="b3ab1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ab1-103">Остановка задания HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="b3ab1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3ab1-104">SYNTAX</span></span>

### <span data-ttu-id="b3ab1-105">Запуск jobDetails на кластере HDInsight (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3ab1-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3ab1-106">Запуск jobDetails в кластере HDInsight (с определенными учетными данными подписки)</span><span class="sxs-lookup"><span data-stu-id="b3ab1-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b3ab1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3ab1-107">DESCRIPTION</span></span>
<span data-ttu-id="b3ab1-108">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b3ab1-109">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b3ab1-110">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b3ab1-111">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b3ab1-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b3ab1-112">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="b3ab1-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b3ab1-113">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b3ab1-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b3ab1-114">Командлет **Stop-AzureHDInsightJob** останавливает задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="b3ab1-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3ab1-115">EXAMPLES</span></span>

## <span data-ttu-id="b3ab1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3ab1-116">PARAMETERS</span></span>

### <span data-ttu-id="b3ab1-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="b3ab1-117">-Certificate</span></span>
<span data-ttu-id="b3ab1-118">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-118">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="b3ab1-119">-Cluster</span></span>
<span data-ttu-id="b3ab1-120">Указывает кластер.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-120">Specifies a cluster.</span></span>
<span data-ttu-id="b3ab1-121">Этот командлет останавливает задание, которое выполняется в кластере, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="b3ab1-122">-Credential</span></span>
<span data-ttu-id="b3ab1-123">Указывает учетные данные, которые следует использовать для прямого доступа по протоколу HTTP к кластеру.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="b3ab1-124">Вы можете указать этот параметр вместо параметра *подписки* для проверки подлинности доступа к кластеру.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-125">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="b3ab1-125">-Endpoint</span></span>
<span data-ttu-id="b3ab1-126">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b3ab1-127">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b3ab1-128">-HostedService</span></span>
<span data-ttu-id="b3ab1-129">Указывает пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b3ab1-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="b3ab1-131">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="b3ab1-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="b3ab1-132">-JobId</span></span>
<span data-ttu-id="b3ab1-133">Указывает ИД задания HDInsight, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="b3ab1-134">-Profile</span></span>
<span data-ttu-id="b3ab1-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3ab1-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3ab1-137">-Подписка</span><span class="sxs-lookup"><span data-stu-id="b3ab1-137">-Subscription</span></span>
<span data-ttu-id="b3ab1-138">Указывает подписку.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-138">Specifies a subscription.</span></span>
<span data-ttu-id="b3ab1-139">Этот командлет останавливает задание для подписки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ab1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ab1-140">CommonParameters</span></span>
<span data-ttu-id="b3ab1-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ab1-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ab1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ab1-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3ab1-143">INPUTS</span></span>

## <span data-ttu-id="b3ab1-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3ab1-144">OUTPUTS</span></span>

## <span data-ttu-id="b3ab1-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3ab1-145">NOTES</span></span>

## <span data-ttu-id="b3ab1-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3ab1-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3ab1-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b3ab1-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="b3ab1-148">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b3ab1-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="b3ab1-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b3ab1-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


