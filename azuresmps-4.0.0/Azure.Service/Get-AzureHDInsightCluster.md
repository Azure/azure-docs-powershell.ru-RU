---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075644"
---
# <span data-ttu-id="872df-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="872df-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="872df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="872df-102">SYNOPSIS</span></span>
<span data-ttu-id="872df-103">Возвращает кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="872df-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="872df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="872df-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="872df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="872df-105">DESCRIPTION</span></span>
<span data-ttu-id="872df-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="872df-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="872df-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="872df-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="872df-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="872df-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="872df-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="872df-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="872df-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="872df-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="872df-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="872df-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="872df-112">Командлет **Get-AzureHDInsightCluster** получает кластеры служб Azure HDInsight для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="872df-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="872df-113">Вы можете использовать параметр *Name* для получения определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="872df-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="872df-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="872df-114">EXAMPLES</span></span>

### <span data-ttu-id="872df-115">Пример 1: получение кластеров в подписке</span><span class="sxs-lookup"><span data-stu-id="872df-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="872df-116">Эта команда получает сведения о кластерах HDInsight в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="872df-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="872df-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="872df-117">PARAMETERS</span></span>

### <span data-ttu-id="872df-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="872df-118">-Certificate</span></span>
<span data-ttu-id="872df-119">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="872df-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="872df-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="872df-120">-Endpoint</span></span>
<span data-ttu-id="872df-121">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="872df-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="872df-122">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="872df-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="872df-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="872df-123">-HostedService</span></span>
<span data-ttu-id="872df-124">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="872df-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="872df-125">Если этот параметр не указан, этот командлет использует пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="872df-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="872df-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="872df-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="872df-127">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="872df-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="872df-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="872df-128">-Name</span></span>
<span data-ttu-id="872df-129">Указывает имя получаемого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="872df-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="872df-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="872df-130">-Profile</span></span>
<span data-ttu-id="872df-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="872df-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="872df-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="872df-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="872df-133">-Подписка</span><span class="sxs-lookup"><span data-stu-id="872df-133">-Subscription</span></span>
<span data-ttu-id="872df-134">Указывает подписку, которая содержит кластер HDInsight для получения.</span><span class="sxs-lookup"><span data-stu-id="872df-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="872df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872df-135">CommonParameters</span></span>
<span data-ttu-id="872df-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="872df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872df-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872df-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="872df-138">INPUTS</span></span>

## <span data-ttu-id="872df-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="872df-139">OUTPUTS</span></span>

## <span data-ttu-id="872df-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="872df-140">NOTES</span></span>

## <span data-ttu-id="872df-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="872df-141">RELATED LINKS</span></span>

[<span data-ttu-id="872df-142">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="872df-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="872df-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="872df-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="872df-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="872df-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


