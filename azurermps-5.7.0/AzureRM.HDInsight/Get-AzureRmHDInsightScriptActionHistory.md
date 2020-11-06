---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: b2e302f9490cb5671728a46105ad574b54270c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557352"
---
# <span data-ttu-id="b1b73-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="b1b73-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="b1b73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1b73-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b73-103">Получает журнал действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="b1b73-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1b73-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1b73-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b73-106">Командлет **Get-AzureRmHDInsightScriptActionHistory** получает журнал действий сценария для кластера Azure HDInsight и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="b1b73-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="b1b73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1b73-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b73-108">Пример 1: получение истории выполнения действий сценария для кластера</span><span class="sxs-lookup"><span data-stu-id="b1b73-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b1b73-109">Эта команда получает историю действий сценария для кластера, в котором установлен-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b1b73-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="b1b73-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1b73-110">PARAMETERS</span></span>

### <span data-ttu-id="b1b73-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b1b73-111">-ClusterName</span></span>
<span data-ttu-id="b1b73-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b1b73-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b1b73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b73-113">-DefaultProfile</span></span>
<span data-ttu-id="b1b73-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1b73-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1b73-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b73-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1b73-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1b73-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b1b73-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="b1b73-117">-ScriptExecutionId</span></span>
<span data-ttu-id="b1b73-118">Указывает идентификатор выполнения действия выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="b1b73-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b73-119">CommonParameters</span></span>
<span data-ttu-id="b1b73-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1b73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b73-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b73-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b73-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1b73-122">INPUTS</span></span>

### <span data-ttu-id="b1b73-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="b1b73-123">None</span></span>
<span data-ttu-id="b1b73-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b1b73-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1b73-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1b73-125">OUTPUTS</span></span>

### <span data-ttu-id="b1b73-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="b1b73-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="b1b73-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1b73-127">NOTES</span></span>

## <span data-ttu-id="b1b73-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1b73-128">RELATED LINKS</span></span>

