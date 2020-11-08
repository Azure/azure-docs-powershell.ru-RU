---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076262"
---
# <span data-ttu-id="ff346-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="ff346-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="ff346-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff346-102">SYNOPSIS</span></span>
<span data-ttu-id="ff346-103">Предоставляет доступ к кластеру HDInsight через RDP.</span><span class="sxs-lookup"><span data-stu-id="ff346-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="ff346-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff346-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff346-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff346-105">DESCRIPTION</span></span>
<span data-ttu-id="ff346-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="ff346-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ff346-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="ff346-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ff346-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff346-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ff346-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ff346-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ff346-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ff346-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ff346-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff346-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ff346-112">Командлет **Grant-AzureHDInsightRdpAccess** предоставляет протоколу удаленного рабочего стола доступ к кластеру HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="ff346-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ff346-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff346-113">EXAMPLES</span></span>

## <span data-ttu-id="ff346-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff346-114">PARAMETERS</span></span>

### <span data-ttu-id="ff346-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ff346-115">-Certificate</span></span>
<span data-ttu-id="ff346-116">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ff346-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ff346-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="ff346-117">-Endpoint</span></span>
<span data-ttu-id="ff346-118">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="ff346-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ff346-119">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff346-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ff346-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ff346-120">-HostedService</span></span>
<span data-ttu-id="ff346-121">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff346-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="ff346-122">Если этот параметр не указан, этот командлет использует пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff346-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="ff346-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ff346-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="ff346-124">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="ff346-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ff346-125">-Location</span><span class="sxs-lookup"><span data-stu-id="ff346-125">-Location</span></span>
<span data-ttu-id="ff346-126">Указывает область Azure, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="ff346-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="ff346-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff346-127">-Name</span></span>
<span data-ttu-id="ff346-128">Указывает имя кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff346-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="ff346-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="ff346-129">-Profile</span></span>
<span data-ttu-id="ff346-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff346-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff346-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff346-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff346-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ff346-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="ff346-133">Задает срок действия в виде объекта **DateTime** для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="ff346-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff346-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ff346-134">-RdpCredential</span></span>
<span data-ttu-id="ff346-135">Указывает учетные данные для доступа к кластеру по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="ff346-135">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff346-136">-Подписка</span><span class="sxs-lookup"><span data-stu-id="ff346-136">-Subscription</span></span>
<span data-ttu-id="ff346-137">Указывает подписку, которая содержит кластер HDInsight, которому нужно предоставить доступ.</span><span class="sxs-lookup"><span data-stu-id="ff346-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="ff346-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff346-138">CommonParameters</span></span>
<span data-ttu-id="ff346-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff346-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff346-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff346-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff346-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff346-141">INPUTS</span></span>

## <span data-ttu-id="ff346-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff346-142">OUTPUTS</span></span>

## <span data-ttu-id="ff346-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff346-143">NOTES</span></span>

## <span data-ttu-id="ff346-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff346-144">RELATED LINKS</span></span>

[<span data-ttu-id="ff346-145">REVOKE-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="ff346-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


