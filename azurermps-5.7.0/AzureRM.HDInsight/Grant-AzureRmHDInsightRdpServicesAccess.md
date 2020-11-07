---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732372"
---
# <span data-ttu-id="fb693-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fb693-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="fb693-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb693-102">SYNOPSIS</span></span>
<span data-ttu-id="fb693-103">Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="fb693-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb693-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb693-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb693-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb693-105">DESCRIPTION</span></span>
<span data-ttu-id="fb693-106">Командлет **Grant-AzureRmHDInsightRdpServicesAccess** включает протокол удаленного рабочего стола (RDP) для доступа к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="fb693-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fb693-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb693-107">EXAMPLES</span></span>

### <span data-ttu-id="fb693-108">Пример 1: предоставление доступа к удаленному рабочему столу в кластере HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="fb693-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="fb693-109">Эта команда предоставляет доступ к кластеру через RDP с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="fb693-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="fb693-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb693-110">PARAMETERS</span></span>

### <span data-ttu-id="fb693-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="fb693-111">-ClusterName</span></span>
<span data-ttu-id="fb693-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="fb693-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb693-113">-DefaultProfile</span></span>
<span data-ttu-id="fb693-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fb693-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb693-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="fb693-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="fb693-116">Задает срок действия в виде объекта **DateTime** для доступа к кластеру по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="fb693-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb693-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="fb693-117">-RdpCredential</span></span>
<span data-ttu-id="fb693-118">Указывает учетные данные RDP для кластера.</span><span class="sxs-lookup"><span data-stu-id="fb693-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="fb693-119">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="fb693-119">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb693-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb693-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb693-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb693-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb693-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb693-122">CommonParameters</span></span>
<span data-ttu-id="fb693-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb693-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb693-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb693-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb693-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb693-125">INPUTS</span></span>

### <span data-ttu-id="fb693-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="fb693-126">None</span></span>
<span data-ttu-id="fb693-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fb693-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb693-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb693-128">OUTPUTS</span></span>

### <span data-ttu-id="fb693-129">System. void</span><span class="sxs-lookup"><span data-stu-id="fb693-129">System.Void</span></span>

## <span data-ttu-id="fb693-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb693-130">NOTES</span></span>

## <span data-ttu-id="fb693-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb693-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb693-132">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fb693-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


