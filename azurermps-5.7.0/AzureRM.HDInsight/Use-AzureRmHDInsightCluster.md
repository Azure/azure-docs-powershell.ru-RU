---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: c8a58963e66c8260a0001c144230cabf3a80b295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734715"
---
# <span data-ttu-id="eb683-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eb683-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="eb683-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb683-102">SYNOPSIS</span></span>
<span data-ttu-id="eb683-103">Выбор кластера для использования с командлетом Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="eb683-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb683-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb683-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb683-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb683-105">DESCRIPTION</span></span>
<span data-ttu-id="eb683-106">Командлет **use-AzureRmHDInsightCluster** выбирает кластер Azure HDInsight для командлета Invoke-AzureRmHDInsightHiveJob, который будет использоваться для отправки заданий Hive.</span><span class="sxs-lookup"><span data-stu-id="eb683-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="eb683-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb683-107">EXAMPLES</span></span>

### <span data-ttu-id="eb683-108">Пример 1: выбор кластера для отправки запроса куста</span><span class="sxs-lookup"><span data-stu-id="eb683-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="eb683-109">Эта команда позволяет выбрать кластер для отправки запроса куста.</span><span class="sxs-lookup"><span data-stu-id="eb683-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="eb683-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb683-110">PARAMETERS</span></span>

### <span data-ttu-id="eb683-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="eb683-111">-ClusterName</span></span>
<span data-ttu-id="eb683-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="eb683-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="eb683-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb683-113">-DefaultProfile</span></span>
<span data-ttu-id="eb683-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb683-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb683-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="eb683-115">-HttpCredential</span></span>
<span data-ttu-id="eb683-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="eb683-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb683-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb683-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb683-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb683-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eb683-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb683-119">CommonParameters</span></span>
<span data-ttu-id="eb683-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb683-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb683-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb683-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb683-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb683-122">INPUTS</span></span>

### <span data-ttu-id="eb683-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb683-123">None</span></span>
<span data-ttu-id="eb683-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb683-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb683-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb683-125">OUTPUTS</span></span>

### <span data-ttu-id="eb683-126">System. String</span><span class="sxs-lookup"><span data-stu-id="eb683-126">System.String</span></span>

## <span data-ttu-id="eb683-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb683-127">NOTES</span></span>

## <span data-ttu-id="eb683-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb683-128">RELATED LINKS</span></span>

[<span data-ttu-id="eb683-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eb683-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="eb683-130">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eb683-130">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


