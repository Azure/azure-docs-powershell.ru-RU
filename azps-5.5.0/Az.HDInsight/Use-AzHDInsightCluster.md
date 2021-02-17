---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: a4e02a10bef16fad21a44ca7952a5f2e429846d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219921"
---
# <span data-ttu-id="eec12-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eec12-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="eec12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec12-102">SYNOPSIS</span></span>
<span data-ttu-id="eec12-103">Выбирает кластер, который будет использоваться с Invoke-RmAzureHDInsightHiveJob управления.</span><span class="sxs-lookup"><span data-stu-id="eec12-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="eec12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eec12-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eec12-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eec12-105">DESCRIPTION</span></span>
<span data-ttu-id="eec12-106">Для **этого с** помощью Invoke-AzHDInsightHiveJob Azure HDInsight выбирается кластер Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eec12-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="eec12-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eec12-107">EXAMPLES</span></span>

### <span data-ttu-id="eec12-108">Пример 1. Выбор кластера для отправки запроса "Блок"</span><span class="sxs-lookup"><span data-stu-id="eec12-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="eec12-109">Эта команда выбирает кластер для отправки запроса "Блок".</span><span class="sxs-lookup"><span data-stu-id="eec12-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="eec12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eec12-110">PARAMETERS</span></span>

### <span data-ttu-id="eec12-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eec12-111">-ClusterName</span></span>
<span data-ttu-id="eec12-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="eec12-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="eec12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec12-113">-DefaultProfile</span></span>
<span data-ttu-id="eec12-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eec12-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eec12-115">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="eec12-115">-HttpCredential</span></span>
<span data-ttu-id="eec12-116">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="eec12-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="eec12-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec12-117">-ResourceGroupName</span></span>
<span data-ttu-id="eec12-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eec12-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eec12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec12-119">CommonParameters</span></span>
<span data-ttu-id="eec12-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec12-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eec12-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec12-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eec12-122">INPUTS</span></span>

### <span data-ttu-id="eec12-123">Нет</span><span class="sxs-lookup"><span data-stu-id="eec12-123">None</span></span>

## <span data-ttu-id="eec12-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eec12-124">OUTPUTS</span></span>

### <span data-ttu-id="eec12-125">System.String</span><span class="sxs-lookup"><span data-stu-id="eec12-125">System.String</span></span>

## <span data-ttu-id="eec12-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eec12-126">NOTES</span></span>

## <span data-ttu-id="eec12-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eec12-127">RELATED LINKS</span></span>

[<span data-ttu-id="eec12-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eec12-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="eec12-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eec12-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


