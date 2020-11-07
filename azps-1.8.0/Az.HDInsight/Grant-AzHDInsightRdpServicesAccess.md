---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900486"
---
# <span data-ttu-id="6bb0c-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6bb0c-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="6bb0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb0c-103">Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="6bb0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bb0c-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bb0c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb0c-106">Командлет **Grant-AzHDInsightRdpServicesAccess** включает протокол удаленного рабочего стола (RDP) для доступа к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6bb0c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb0c-108">Пример 1: предоставление доступа к удаленному рабочему столу в кластере HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="6bb0c-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="6bb0c-109">Эта команда предоставляет доступ к кластеру через RDP с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6bb0c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-110">PARAMETERS</span></span>

### <span data-ttu-id="6bb0c-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="6bb0c-111">-ClusterName</span></span>
<span data-ttu-id="6bb0c-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb0c-113">-DefaultProfile</span></span>
<span data-ttu-id="6bb0c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6bb0c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="6bb0c-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="6bb0c-116">Задает срок действия в виде объекта **DateTime** для доступа к кластеру по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6bb0c-117">-RdpCredential</span></span>
<span data-ttu-id="6bb0c-118">Указывает учетные данные RDP для кластера.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="6bb0c-119">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-119">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6bb0c-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-121">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb0c-122">CommonParameters</span></span>
<span data-ttu-id="6bb0c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb0c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb0c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb0c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bb0c-125">INPUTS</span></span>

### <span data-ttu-id="6bb0c-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="6bb0c-126">None</span></span>

## <span data-ttu-id="6bb0c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-127">OUTPUTS</span></span>

### <span data-ttu-id="6bb0c-128">System. void</span><span class="sxs-lookup"><span data-stu-id="6bb0c-128">System.Void</span></span>

## <span data-ttu-id="6bb0c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bb0c-129">NOTES</span></span>

## <span data-ttu-id="6bb0c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-130">RELATED LINKS</span></span>

[<span data-ttu-id="6bb0c-131">REVOKE-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6bb0c-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


