---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076351"
---
# <span data-ttu-id="49d73-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="49d73-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="49d73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49d73-102">SYNOPSIS</span></span>
<span data-ttu-id="49d73-103">Возвращает свойства, специфичные для службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="49d73-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="49d73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49d73-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="49d73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49d73-105">DESCRIPTION</span></span>
<span data-ttu-id="49d73-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="49d73-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="49d73-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="49d73-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="49d73-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="49d73-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="49d73-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="49d73-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="49d73-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="49d73-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="49d73-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="49d73-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="49d73-112">Командлет **Get-AzureHDInsightProperties** получает свойства, специфические для службы HDInsight Azure, например список доступных областей Azure, версий кластера HDInsight и доступной вычислительной мощности.</span><span class="sxs-lookup"><span data-stu-id="49d73-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="49d73-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49d73-113">EXAMPLES</span></span>

### <span data-ttu-id="49d73-114">Пример 1: получение свойств HDInsight для подписки</span><span class="sxs-lookup"><span data-stu-id="49d73-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="49d73-115">Первая команда получает имя текущей подписки Azure, а затем сохраняет ее в переменной $SubName.</span><span class="sxs-lookup"><span data-stu-id="49d73-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="49d73-116">Вторая команда получает свойства HDInsight для подписки в $SubName.</span><span class="sxs-lookup"><span data-stu-id="49d73-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="49d73-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49d73-117">PARAMETERS</span></span>

### <span data-ttu-id="49d73-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="49d73-118">-Certificate</span></span>
<span data-ttu-id="49d73-119">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="49d73-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="49d73-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="49d73-120">-Endpoint</span></span>
<span data-ttu-id="49d73-121">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="49d73-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="49d73-122">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49d73-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="49d73-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="49d73-123">-HostedService</span></span>
<span data-ttu-id="49d73-124">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="49d73-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="49d73-125">Если этот параметр не указан, этот командлет использует пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49d73-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="49d73-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="49d73-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="49d73-127">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="49d73-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="49d73-128">-Расположения</span><span class="sxs-lookup"><span data-stu-id="49d73-128">-Locations</span></span>
<span data-ttu-id="49d73-129">Указывает, что этот командлет получает список областей Azure, в которых доступна служба HDInsight.</span><span class="sxs-lookup"><span data-stu-id="49d73-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d73-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="49d73-130">-Profile</span></span>
<span data-ttu-id="49d73-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="49d73-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49d73-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49d73-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49d73-133">-Подписка</span><span class="sxs-lookup"><span data-stu-id="49d73-133">-Subscription</span></span>
<span data-ttu-id="49d73-134">Указывает подписку, которая содержит свойства HDInsight для получения.</span><span class="sxs-lookup"><span data-stu-id="49d73-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="49d73-135">-Versions</span><span class="sxs-lookup"><span data-stu-id="49d73-135">-Versions</span></span>
<span data-ttu-id="49d73-136">Указывает на то, что этот командлет получает список версий кластера HDInsight, доступных в службе для подписки.</span><span class="sxs-lookup"><span data-stu-id="49d73-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d73-137">CommonParameters</span></span>
<span data-ttu-id="49d73-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49d73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d73-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d73-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d73-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49d73-140">INPUTS</span></span>

## <span data-ttu-id="49d73-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49d73-141">OUTPUTS</span></span>

## <span data-ttu-id="49d73-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="49d73-142">NOTES</span></span>

## <span data-ttu-id="49d73-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49d73-143">RELATED LINKS</span></span>

