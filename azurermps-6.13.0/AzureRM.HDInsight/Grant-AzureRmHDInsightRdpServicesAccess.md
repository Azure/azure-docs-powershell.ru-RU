---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: ce169dc1cce1552b48aa864885c6877624da0176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563032"
---
# <span data-ttu-id="3fadd-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3fadd-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="3fadd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fadd-102">SYNOPSIS</span></span>
<span data-ttu-id="3fadd-103">Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="3fadd-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fadd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fadd-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fadd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fadd-105">DESCRIPTION</span></span>
<span data-ttu-id="3fadd-106">Командлет **Grant-AzureRmHDInsightRdpServicesAccess** включает протокол удаленного рабочего стола (RDP) для доступа к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="3fadd-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3fadd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fadd-107">EXAMPLES</span></span>

### <span data-ttu-id="3fadd-108">Пример 1: предоставление доступа к удаленному рабочему столу в кластере HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="3fadd-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="3fadd-109">Эта команда предоставляет доступ к кластеру через RDP с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="3fadd-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3fadd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fadd-110">PARAMETERS</span></span>

### <span data-ttu-id="3fadd-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="3fadd-111">-ClusterName</span></span>
<span data-ttu-id="3fadd-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="3fadd-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3fadd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fadd-113">-DefaultProfile</span></span>
<span data-ttu-id="3fadd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3fadd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="3fadd-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="3fadd-116">Задает срок действия в виде объекта **DateTime** для доступа к кластеру по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="3fadd-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="3fadd-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="3fadd-117">-RdpCredential</span></span>
<span data-ttu-id="3fadd-118">Указывает учетные данные RDP для кластера.</span><span class="sxs-lookup"><span data-stu-id="3fadd-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="3fadd-119">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="3fadd-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="3fadd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fadd-120">-ResourceGroupName</span></span>
<span data-ttu-id="3fadd-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fadd-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3fadd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fadd-122">CommonParameters</span></span>
<span data-ttu-id="3fadd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fadd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fadd-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fadd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fadd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fadd-125">INPUTS</span></span>

### <span data-ttu-id="3fadd-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="3fadd-126">None</span></span>

## <span data-ttu-id="3fadd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fadd-127">OUTPUTS</span></span>

### <span data-ttu-id="3fadd-128">System. void</span><span class="sxs-lookup"><span data-stu-id="3fadd-128">System.Void</span></span>

## <span data-ttu-id="3fadd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fadd-129">NOTES</span></span>

## <span data-ttu-id="3fadd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fadd-130">RELATED LINKS</span></span>

[<span data-ttu-id="3fadd-131">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3fadd-131">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


