---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: c89293ee071aba3fcec2d58d071714193cc44a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010483"
---
# <span data-ttu-id="5ffc3-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5ffc3-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="5ffc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ffc3-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffc3-103">Возвращает и перечисляет все кластеры Azure HDInsight, связанные с текущей подпиской или определенной группой ресурсов, либо извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="5ffc3-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="5ffc3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ffc3-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ffc3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ffc3-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffc3-106">Для текущей подписки на Azure HDInsight перечислены кластеры службы **Get-AzHDInsightCluster.**</span><span class="sxs-lookup"><span data-stu-id="5ffc3-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="5ffc3-107">Используйте параметр *ClusterName* для получения сведений о конкретном кластере.</span><span class="sxs-lookup"><span data-stu-id="5ffc3-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="5ffc3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ffc3-108">EXAMPLES</span></span>

### <span data-ttu-id="5ffc3-109">Пример 1. Список всех кластеров Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="5ffc3-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="5ffc3-110">Эта команда содержит список всех кластеров Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5ffc3-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="5ffc3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ffc3-111">PARAMETERS</span></span>

### <span data-ttu-id="5ffc3-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5ffc3-112">-ClusterName</span></span>
<span data-ttu-id="5ffc3-113">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="5ffc3-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffc3-114">-DefaultProfile</span></span>
<span data-ttu-id="5ffc3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ffc3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ffc3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffc3-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ffc3-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ffc3-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffc3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffc3-118">CommonParameters</span></span>
<span data-ttu-id="5ffc3-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffc3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffc3-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ffc3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffc3-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffc3-121">INPUTS</span></span>

### <span data-ttu-id="5ffc3-122">Нет</span><span class="sxs-lookup"><span data-stu-id="5ffc3-122">None</span></span>

## <span data-ttu-id="5ffc3-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffc3-123">OUTPUTS</span></span>

### <span data-ttu-id="5ffc3-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5ffc3-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="5ffc3-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ffc3-125">NOTES</span></span>

## <span data-ttu-id="5ffc3-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ffc3-126">RELATED LINKS</span></span>

[<span data-ttu-id="5ffc3-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5ffc3-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="5ffc3-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5ffc3-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


