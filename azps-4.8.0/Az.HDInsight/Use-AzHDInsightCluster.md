---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079616"
---
# <span data-ttu-id="20b95-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20b95-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="20b95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20b95-102">SYNOPSIS</span></span>
<span data-ttu-id="20b95-103">Выбор кластера для использования с командлетом Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="20b95-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="20b95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20b95-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20b95-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20b95-105">DESCRIPTION</span></span>
<span data-ttu-id="20b95-106">Командлет **use-AzHDInsightCluster** выбирает кластер Azure HDInsight для командлета Invoke-AzHDInsightHiveJob, который будет использоваться для отправки заданий Hive.</span><span class="sxs-lookup"><span data-stu-id="20b95-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="20b95-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20b95-107">EXAMPLES</span></span>

### <span data-ttu-id="20b95-108">Пример 1: выбор кластера для отправки запроса куста</span><span class="sxs-lookup"><span data-stu-id="20b95-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="20b95-109">Эта команда позволяет выбрать кластер для отправки запроса куста.</span><span class="sxs-lookup"><span data-stu-id="20b95-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="20b95-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20b95-110">PARAMETERS</span></span>

### <span data-ttu-id="20b95-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="20b95-111">-ClusterName</span></span>
<span data-ttu-id="20b95-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="20b95-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="20b95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b95-113">-DefaultProfile</span></span>
<span data-ttu-id="20b95-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20b95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20b95-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="20b95-115">-HttpCredential</span></span>
<span data-ttu-id="20b95-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="20b95-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="20b95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b95-117">-ResourceGroupName</span></span>
<span data-ttu-id="20b95-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20b95-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="20b95-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b95-119">CommonParameters</span></span>
<span data-ttu-id="20b95-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20b95-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b95-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b95-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b95-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20b95-122">INPUTS</span></span>

### <span data-ttu-id="20b95-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="20b95-123">None</span></span>

## <span data-ttu-id="20b95-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20b95-124">OUTPUTS</span></span>

### <span data-ttu-id="20b95-125">System. String</span><span class="sxs-lookup"><span data-stu-id="20b95-125">System.String</span></span>

## <span data-ttu-id="20b95-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="20b95-126">NOTES</span></span>

## <span data-ttu-id="20b95-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20b95-127">RELATED LINKS</span></span>

[<span data-ttu-id="20b95-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20b95-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="20b95-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20b95-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


