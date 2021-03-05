---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 136099b4fb37952825afbf82ba99a11695b901a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009107"
---
# <span data-ttu-id="7e159-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="7e159-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="7e159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e159-102">SYNOPSIS</span></span>
<span data-ttu-id="7e159-103">Возвращает неупорядоченные действия сценариев для кластера и перечисляет их в хронологическом порядке или получает сведения об указанном действии сохраняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="7e159-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="7e159-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e159-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e159-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e159-105">DESCRIPTION</span></span>
<span data-ttu-id="7e159-106">При этом сохраняются действия сценария для кластера Azure **HDInsightPersistedScriptAction** и перечислены в хронологическом порядке, а также подробные сведения об указанном действии сохраняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="7e159-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="7e159-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e159-107">EXAMPLES</span></span>

### <span data-ttu-id="7e159-108">Пример 1. Просмотр сохраняемой группы действий сценария</span><span class="sxs-lookup"><span data-stu-id="7e159-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="7e159-109">Эта команда сохраняется в кластере под названием "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="7e159-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7e159-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e159-110">PARAMETERS</span></span>

### <span data-ttu-id="7e159-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7e159-111">-ClusterName</span></span>
<span data-ttu-id="7e159-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="7e159-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7e159-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e159-113">-DefaultProfile</span></span>
<span data-ttu-id="7e159-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e159-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e159-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7e159-115">-Name</span></span>
<span data-ttu-id="7e159-116">Указывает имя сохраняемого действия сценария.</span><span class="sxs-lookup"><span data-stu-id="7e159-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="7e159-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e159-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e159-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e159-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7e159-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e159-119">CommonParameters</span></span>
<span data-ttu-id="7e159-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e159-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e159-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e159-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e159-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e159-122">INPUTS</span></span>

### <span data-ttu-id="7e159-123">Нет</span><span class="sxs-lookup"><span data-stu-id="7e159-123">None</span></span>

## <span data-ttu-id="7e159-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e159-124">OUTPUTS</span></span>

### <span data-ttu-id="7e159-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="7e159-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="7e159-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e159-126">NOTES</span></span>

## <span data-ttu-id="7e159-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e159-127">RELATED LINKS</span></span>

[<span data-ttu-id="7e159-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="7e159-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="7e159-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="7e159-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


