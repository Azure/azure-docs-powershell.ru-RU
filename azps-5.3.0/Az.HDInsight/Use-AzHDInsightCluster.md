---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: a4e02a10bef16fad21a44ca7952a5f2e429846d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504802"
---
# <span data-ttu-id="f6971-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f6971-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="f6971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6971-102">SYNOPSIS</span></span>
<span data-ttu-id="f6971-103">Выбирает кластер, который будет использоваться с Invoke-RmAzureHDInsightHiveJob..</span><span class="sxs-lookup"><span data-stu-id="f6971-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="f6971-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6971-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6971-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6971-105">DESCRIPTION</span></span>
<span data-ttu-id="f6971-106">Для **этого с** помощью Invoke-AzHDInsightHiveJob Azure HDInsight выбирается кластер Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f6971-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="f6971-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6971-107">EXAMPLES</span></span>

### <span data-ttu-id="f6971-108">Пример 1. Выбор кластера для отправки запроса "Блок"</span><span class="sxs-lookup"><span data-stu-id="f6971-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f6971-109">Эта команда выбирает кластер для отправки запроса "Блок".</span><span class="sxs-lookup"><span data-stu-id="f6971-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="f6971-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6971-110">PARAMETERS</span></span>

### <span data-ttu-id="f6971-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f6971-111">-ClusterName</span></span>
<span data-ttu-id="f6971-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="f6971-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f6971-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6971-113">-DefaultProfile</span></span>
<span data-ttu-id="f6971-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6971-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6971-115">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="f6971-115">-HttpCredential</span></span>
<span data-ttu-id="f6971-116">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="f6971-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6971-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6971-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6971-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6971-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6971-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6971-119">CommonParameters</span></span>
<span data-ttu-id="f6971-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6971-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6971-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6971-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6971-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6971-122">INPUTS</span></span>

### <span data-ttu-id="f6971-123">Нет</span><span class="sxs-lookup"><span data-stu-id="f6971-123">None</span></span>

## <span data-ttu-id="f6971-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6971-124">OUTPUTS</span></span>

### <span data-ttu-id="f6971-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f6971-125">System.String</span></span>

## <span data-ttu-id="f6971-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6971-126">NOTES</span></span>

## <span data-ttu-id="f6971-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6971-127">RELATED LINKS</span></span>

[<span data-ttu-id="f6971-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f6971-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="f6971-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f6971-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


