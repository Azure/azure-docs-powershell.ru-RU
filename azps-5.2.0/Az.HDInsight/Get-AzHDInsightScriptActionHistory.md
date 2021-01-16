---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 4f73c58ee709e53e1337c161b698aa31cc38ca43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396591"
---
# <span data-ttu-id="65043-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="65043-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="65043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65043-102">SYNOPSIS</span></span>
<span data-ttu-id="65043-103">Получает историю действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="65043-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="65043-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65043-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65043-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65043-105">DESCRIPTION</span></span>
<span data-ttu-id="65043-106">Cmdlet **Get-AzHDInsightScriptActionHistory** получает историю действий сценария для кластера Azure HDInsight и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="65043-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="65043-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65043-107">EXAMPLES</span></span>

### <span data-ttu-id="65043-108">Пример 1. Просмотр истории выполнения действий сценария для кластера</span><span class="sxs-lookup"><span data-stu-id="65043-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="65043-109">Эта команда получает историю действий сценариев для кластера your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="65043-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="65043-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65043-110">PARAMETERS</span></span>

### <span data-ttu-id="65043-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="65043-111">-ClusterName</span></span>
<span data-ttu-id="65043-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="65043-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="65043-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65043-113">-DefaultProfile</span></span>
<span data-ttu-id="65043-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="65043-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65043-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65043-115">-ResourceGroupName</span></span>
<span data-ttu-id="65043-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65043-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="65043-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="65043-117">-ScriptExecutionId</span></span>
<span data-ttu-id="65043-118">Определяет ид выполнения действия, выполненного сценарием.</span><span class="sxs-lookup"><span data-stu-id="65043-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65043-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65043-119">CommonParameters</span></span>
<span data-ttu-id="65043-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65043-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65043-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65043-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65043-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65043-122">INPUTS</span></span>

### <span data-ttu-id="65043-123">Нет</span><span class="sxs-lookup"><span data-stu-id="65043-123">None</span></span>

## <span data-ttu-id="65043-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65043-124">OUTPUTS</span></span>

### <span data-ttu-id="65043-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="65043-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="65043-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65043-126">NOTES</span></span>

## <span data-ttu-id="65043-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65043-127">RELATED LINKS</span></span>
