---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076350"
---
# <span data-ttu-id="23d9d-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="23d9d-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="23d9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="23d9d-103">Возвращает задания HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23d9d-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="23d9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23d9d-104">SYNTAX</span></span>

### <span data-ttu-id="23d9d-105">Получение журнала jobDetails для кластера HDInsight (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23d9d-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="23d9d-106">Получение журнала jobDetails для кластера HDInsight (с определенными учетными данными подписки)</span><span class="sxs-lookup"><span data-stu-id="23d9d-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23d9d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="23d9d-108">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="23d9d-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="23d9d-109">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="23d9d-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="23d9d-110">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23d9d-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="23d9d-111">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="23d9d-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="23d9d-112">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="23d9d-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="23d9d-113">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="23d9d-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="23d9d-114">Командлет **Get-AzureHDInsightJob** получает последние задания Azure HDInsight для указанного кластера и отображает их в обратном хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="23d9d-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="23d9d-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23d9d-115">EXAMPLES</span></span>

## <span data-ttu-id="23d9d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23d9d-116">PARAMETERS</span></span>

### <span data-ttu-id="23d9d-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="23d9d-117">-Certificate</span></span>
<span data-ttu-id="23d9d-118">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="23d9d-118">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="23d9d-119">-Cluster</span></span>
<span data-ttu-id="23d9d-120">Указывает кластер.</span><span class="sxs-lookup"><span data-stu-id="23d9d-120">Specifies a cluster.</span></span>
<span data-ttu-id="23d9d-121">Этот командлет получает задания HDInsight, которые выполняются в кластере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="23d9d-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="23d9d-122">-Credential</span></span>
<span data-ttu-id="23d9d-123">Указывает учетные данные, которые следует использовать для прямого доступа по протоколу HTTP к кластеру.</span><span class="sxs-lookup"><span data-stu-id="23d9d-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="23d9d-124">Вы можете указать этот параметр вместо параметра *подписки* для проверки подлинности доступа к кластеру.</span><span class="sxs-lookup"><span data-stu-id="23d9d-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-125">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="23d9d-125">-Endpoint</span></span>
<span data-ttu-id="23d9d-126">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="23d9d-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="23d9d-127">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23d9d-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="23d9d-128">-HostedService</span></span>
<span data-ttu-id="23d9d-129">Указывает пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23d9d-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="23d9d-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="23d9d-131">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="23d9d-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="23d9d-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="23d9d-132">-JobId</span></span>
<span data-ttu-id="23d9d-133">Указывает идентификатор задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="23d9d-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="23d9d-134">-Profile</span></span>
<span data-ttu-id="23d9d-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23d9d-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23d9d-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23d9d-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23d9d-137">-Подписка</span><span class="sxs-lookup"><span data-stu-id="23d9d-137">-Subscription</span></span>
<span data-ttu-id="23d9d-138">Указывает подписку, которая содержит задания HDInsight для получения.</span><span class="sxs-lookup"><span data-stu-id="23d9d-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d9d-139">CommonParameters</span></span>
<span data-ttu-id="23d9d-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23d9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d9d-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d9d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d9d-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23d9d-142">INPUTS</span></span>

## <span data-ttu-id="23d9d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23d9d-143">OUTPUTS</span></span>

## <span data-ttu-id="23d9d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="23d9d-144">NOTES</span></span>

## <span data-ttu-id="23d9d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23d9d-145">RELATED LINKS</span></span>

[<span data-ttu-id="23d9d-146">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="23d9d-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="23d9d-147">Остановить-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="23d9d-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="23d9d-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="23d9d-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


