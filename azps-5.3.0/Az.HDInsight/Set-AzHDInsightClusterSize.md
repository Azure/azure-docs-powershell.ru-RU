---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 7dae5bd29877097b7d0df60feff8bf44977e61f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504813"
---
# <span data-ttu-id="073e0-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="073e0-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="073e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073e0-102">SYNOPSIS</span></span>
<span data-ttu-id="073e0-103">Задает количество узлов рабочих в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="073e0-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="073e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="073e0-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="073e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="073e0-105">DESCRIPTION</span></span>
<span data-ttu-id="073e0-106">Cmdlet **Set-AzHDInsightClusterSize** задает количество узлов рабочих в указанном кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="073e0-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="073e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="073e0-107">EXAMPLES</span></span>

### <span data-ttu-id="073e0-108">Пример 1. Настройка размера указанного кластера</span><span class="sxs-lookup"><span data-stu-id="073e0-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="073e0-109">Эта команда задает размер кластера с именем hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="073e0-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="073e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="073e0-110">PARAMETERS</span></span>

### <span data-ttu-id="073e0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="073e0-111">-ClusterName</span></span>
<span data-ttu-id="073e0-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="073e0-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="073e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073e0-113">-DefaultProfile</span></span>
<span data-ttu-id="073e0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="073e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="073e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="073e0-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="073e0-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="073e0-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="073e0-117">-TargetInstanceCount</span></span>
<span data-ttu-id="073e0-118">Определяет нужное количество узлов рабочих узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="073e0-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073e0-119">CommonParameters</span></span>
<span data-ttu-id="073e0-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073e0-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="073e0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073e0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="073e0-122">INPUTS</span></span>

### <span data-ttu-id="073e0-123">Нет</span><span class="sxs-lookup"><span data-stu-id="073e0-123">None</span></span>

## <span data-ttu-id="073e0-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="073e0-124">OUTPUTS</span></span>

### <span data-ttu-id="073e0-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="073e0-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="073e0-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="073e0-126">NOTES</span></span>

## <span data-ttu-id="073e0-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="073e0-127">RELATED LINKS</span></span>
