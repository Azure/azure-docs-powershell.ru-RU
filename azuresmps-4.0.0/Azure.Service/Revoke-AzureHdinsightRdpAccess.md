---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075476"
---
# <span data-ttu-id="41a9d-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="41a9d-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="41a9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="41a9d-103">Запрещает RDP-доступ к кластеру HDInsight.</span><span class="sxs-lookup"><span data-stu-id="41a9d-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="41a9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41a9d-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="41a9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="41a9d-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="41a9d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="41a9d-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="41a9d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="41a9d-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="41a9d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="41a9d-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="41a9d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="41a9d-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="41a9d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="41a9d-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="41a9d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="41a9d-112">Командлет **REVOKE-AzureHDInsightRdpAccess** отключает доступ к кластеру Azure HDInsight по протоколу удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="41a9d-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="41a9d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41a9d-113">EXAMPLES</span></span>

## <span data-ttu-id="41a9d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41a9d-114">PARAMETERS</span></span>

### <span data-ttu-id="41a9d-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="41a9d-115">-Certificate</span></span>
<span data-ttu-id="41a9d-116">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="41a9d-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="41a9d-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="41a9d-117">-Endpoint</span></span>
<span data-ttu-id="41a9d-118">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="41a9d-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="41a9d-119">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41a9d-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="41a9d-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="41a9d-120">-HostedService</span></span>
<span data-ttu-id="41a9d-121">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="41a9d-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="41a9d-122">Если этот параметр не указан, этот командлет использует пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41a9d-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="41a9d-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="41a9d-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="41a9d-124">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="41a9d-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="41a9d-125">-Location</span><span class="sxs-lookup"><span data-stu-id="41a9d-125">-Location</span></span>
<span data-ttu-id="41a9d-126">Указывает область Azure, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="41a9d-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="41a9d-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41a9d-127">-Name</span></span>
<span data-ttu-id="41a9d-128">Указывает имя кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="41a9d-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="41a9d-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="41a9d-129">-Profile</span></span>
<span data-ttu-id="41a9d-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="41a9d-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41a9d-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41a9d-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41a9d-132">-Подписка</span><span class="sxs-lookup"><span data-stu-id="41a9d-132">-Subscription</span></span>
<span data-ttu-id="41a9d-133">Указывает подписку.</span><span class="sxs-lookup"><span data-stu-id="41a9d-133">Specifies a subscription.</span></span>
<span data-ttu-id="41a9d-134">Этот командлет отклоняет доступ к протоколу RDP для подписки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="41a9d-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="41a9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a9d-135">CommonParameters</span></span>
<span data-ttu-id="41a9d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41a9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a9d-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a9d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a9d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41a9d-138">INPUTS</span></span>

## <span data-ttu-id="41a9d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a9d-139">OUTPUTS</span></span>

## <span data-ttu-id="41a9d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="41a9d-140">NOTES</span></span>

## <span data-ttu-id="41a9d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41a9d-141">RELATED LINKS</span></span>

[<span data-ttu-id="41a9d-142">Grant-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="41a9d-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


