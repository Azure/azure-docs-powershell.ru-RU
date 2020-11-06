---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 22d2f4617e5b8a268de8518695d5217191a211df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569451"
---
# <span data-ttu-id="15b4a-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="15b4a-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="15b4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="15b4a-103">Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="15b4a-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15b4a-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15b4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="15b4a-106">Командлет **Grant-AzureRmHDInsightRdpServicesAccess** включает протокол удаленного рабочего стола (RDP) для доступа к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="15b4a-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="15b4a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="15b4a-108">Пример 1: предоставление доступа к удаленному рабочему столу в кластере HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="15b4a-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="15b4a-109">Эта команда предоставляет доступ к кластеру через RDP с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="15b4a-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="15b4a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="15b4a-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="15b4a-111">-ClusterName</span></span>
<span data-ttu-id="15b4a-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="15b4a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="15b4a-113">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="15b4a-113">-RdpAccessExpiry</span></span>
<span data-ttu-id="15b4a-114">Задает срок действия в виде объекта **DateTime** для доступа к кластеру по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="15b4a-114">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="15b4a-115">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="15b4a-115">-RdpCredential</span></span>
<span data-ttu-id="15b4a-116">Указывает учетные данные RDP для кластера.</span><span class="sxs-lookup"><span data-stu-id="15b4a-116">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="15b4a-117">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="15b4a-117">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="15b4a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b4a-118">-ResourceGroupName</span></span>
<span data-ttu-id="15b4a-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15b4a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="15b4a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b4a-120">-DefaultProfile</span></span>
<span data-ttu-id="15b4a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15b4a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b4a-122">CommonParameters</span></span>
<span data-ttu-id="15b4a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15b4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b4a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b4a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b4a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15b4a-125">INPUTS</span></span>

## <span data-ttu-id="15b4a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15b4a-126">OUTPUTS</span></span>

### <span data-ttu-id="15b4a-127">System. void</span><span class="sxs-lookup"><span data-stu-id="15b4a-127">System.Void</span></span>

## <span data-ttu-id="15b4a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="15b4a-128">NOTES</span></span>

## <span data-ttu-id="15b4a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15b4a-129">RELATED LINKS</span></span>

[<span data-ttu-id="15b4a-130">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="15b4a-130">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


