---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076498"
---
# <span data-ttu-id="8c72b-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c72b-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="8c72b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c72b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c72b-103">Предоставление доступа к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c72b-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="8c72b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c72b-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c72b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c72b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c72b-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="8c72b-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8c72b-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="8c72b-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8c72b-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8c72b-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8c72b-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8c72b-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8c72b-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8c72b-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8c72b-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c72b-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8c72b-112">Командлет **Grant-AzureHDInsightHttpServicesAccess** предоставляет доступ по протоколу HTTP к кластеру HDInsight Azure с помощью ODBC, Ambari, Oozie и веб-служб.</span><span class="sxs-lookup"><span data-stu-id="8c72b-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="8c72b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c72b-113">EXAMPLES</span></span>

## <span data-ttu-id="8c72b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c72b-114">PARAMETERS</span></span>

### <span data-ttu-id="8c72b-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="8c72b-115">-Certificate</span></span>
<span data-ttu-id="8c72b-116">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="8c72b-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="8c72b-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="8c72b-117">-Credential</span></span>
<span data-ttu-id="8c72b-118">Указывает имя пользователя и пароль для доступа по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c72b-118">Specifies a user name and password for HTTP access.</span></span>

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

### <span data-ttu-id="8c72b-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="8c72b-119">-Endpoint</span></span>
<span data-ttu-id="8c72b-120">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="8c72b-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="8c72b-121">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c72b-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="8c72b-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="8c72b-122">-HostedService</span></span>
<span data-ttu-id="8c72b-123">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8c72b-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="8c72b-124">Если этот параметр не указан, этот командлет использует пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c72b-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="8c72b-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="8c72b-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="8c72b-126">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="8c72b-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="8c72b-127">-Location</span><span class="sxs-lookup"><span data-stu-id="8c72b-127">-Location</span></span>
<span data-ttu-id="8c72b-128">Указывает область Azure, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="8c72b-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="8c72b-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c72b-129">-Name</span></span>
<span data-ttu-id="8c72b-130">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="8c72b-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="8c72b-131">Этот командлет предоставляет доступ по протоколу HTTP к кластеру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="8c72b-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c72b-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c72b-132">-Profile</span></span>
<span data-ttu-id="8c72b-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8c72b-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c72b-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c72b-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c72b-135">-Подписка</span><span class="sxs-lookup"><span data-stu-id="8c72b-135">-Subscription</span></span>
<span data-ttu-id="8c72b-136">Указывает подписку, которая содержит кластер HDInsight, которому нужно предоставить доступ.</span><span class="sxs-lookup"><span data-stu-id="8c72b-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="8c72b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c72b-137">CommonParameters</span></span>
<span data-ttu-id="8c72b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c72b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c72b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c72b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c72b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c72b-140">INPUTS</span></span>

## <span data-ttu-id="8c72b-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c72b-141">OUTPUTS</span></span>

## <span data-ttu-id="8c72b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c72b-142">NOTES</span></span>

## <span data-ttu-id="8c72b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c72b-143">RELATED LINKS</span></span>

[<span data-ttu-id="8c72b-144">REVOKE-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c72b-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


