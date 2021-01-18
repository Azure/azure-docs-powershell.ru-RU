---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 344c6fccd0f6c7db26110a94e2cacc53625df3d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504815"
---
# <span data-ttu-id="a9820-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a9820-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a9820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9820-102">SYNOPSIS</span></span>
<span data-ttu-id="a9820-103">Удаляет неуохраняемую действие сценария из кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a9820-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="a9820-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9820-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9820-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9820-105">DESCRIPTION</span></span>
<span data-ttu-id="a9820-106">При настояжении действия сценария **Remove-AzHDInsightPersistedScriptAction** из списка неустанавляемого кластера Azure HDInsight сохраняется действие сценария.</span><span class="sxs-lookup"><span data-stu-id="a9820-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="a9820-107">Удаленный сценарий больше не будет выполняться при масштабе кластера.</span><span class="sxs-lookup"><span data-stu-id="a9820-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="a9820-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9820-108">EXAMPLES</span></span>

### <span data-ttu-id="a9820-109">Пример 1. Удаление действия сценария из списка сохраняемого действия сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="a9820-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="a9820-110">Эта команда удаляет действие scriptaction с именем Scriptaction из списка сохраняемого действия сценария в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="a9820-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="a9820-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9820-111">PARAMETERS</span></span>

### <span data-ttu-id="a9820-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a9820-112">-ClusterName</span></span>
<span data-ttu-id="a9820-113">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="a9820-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a9820-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9820-114">-DefaultProfile</span></span>
<span data-ttu-id="a9820-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9820-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9820-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a9820-116">-Name</span></span>
<span data-ttu-id="a9820-117">Имя сохраняемого действия сценария, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a9820-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9820-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9820-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9820-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9820-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a9820-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9820-120">CommonParameters</span></span>
<span data-ttu-id="a9820-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9820-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9820-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9820-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9820-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9820-123">INPUTS</span></span>

### <span data-ttu-id="a9820-124">Нет</span><span class="sxs-lookup"><span data-stu-id="a9820-124">None</span></span>

## <span data-ttu-id="a9820-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9820-125">OUTPUTS</span></span>

### <span data-ttu-id="a9820-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="a9820-126">System.Void</span></span>

## <span data-ttu-id="a9820-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9820-127">NOTES</span></span>

## <span data-ttu-id="a9820-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9820-128">RELATED LINKS</span></span>

[<span data-ttu-id="a9820-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a9820-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a9820-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a9820-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


