---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 4d3d88fb5a8cca2343403870233e89b0f2073e8e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311843"
---
# <span data-ttu-id="30b46-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="30b46-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="30b46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30b46-102">SYNOPSIS</span></span>
<span data-ttu-id="30b46-103">Удаляет сохраненное действие сценария из кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b46-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="30b46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30b46-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30b46-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30b46-105">DESCRIPTION</span></span>
<span data-ttu-id="30b46-106">Командлет **Remove-AzHDInsightPersistedScriptAction** удаляет сохраненное действие сценария из списка сохраненных действий сценария в Azure HDInsight Cluster.</span><span class="sxs-lookup"><span data-stu-id="30b46-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="30b46-107">Удаленный сценарий больше не будет выполняться при масштабировании кластера.</span><span class="sxs-lookup"><span data-stu-id="30b46-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="30b46-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30b46-108">EXAMPLES</span></span>

### <span data-ttu-id="30b46-109">Пример 1: Удаление действия сценария из списка сохраненных действий сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="30b46-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="30b46-110">Эта команда удаляет действие сценария с именем Scriptaction из списка сохраненных действий сценария в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="30b46-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="30b46-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30b46-111">PARAMETERS</span></span>

### <span data-ttu-id="30b46-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="30b46-112">-ClusterName</span></span>
<span data-ttu-id="30b46-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="30b46-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="30b46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b46-114">-DefaultProfile</span></span>
<span data-ttu-id="30b46-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30b46-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30b46-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30b46-116">-Name</span></span>
<span data-ttu-id="30b46-117">Указывает имя сохраняемого сценария, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="30b46-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="30b46-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b46-118">-ResourceGroupName</span></span>
<span data-ttu-id="30b46-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30b46-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="30b46-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b46-120">CommonParameters</span></span>
<span data-ttu-id="30b46-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30b46-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b46-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30b46-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b46-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30b46-123">INPUTS</span></span>

### <span data-ttu-id="30b46-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="30b46-124">None</span></span>

## <span data-ttu-id="30b46-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30b46-125">OUTPUTS</span></span>

### <span data-ttu-id="30b46-126">System. void</span><span class="sxs-lookup"><span data-stu-id="30b46-126">System.Void</span></span>

## <span data-ttu-id="30b46-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="30b46-127">NOTES</span></span>

## <span data-ttu-id="30b46-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30b46-128">RELATED LINKS</span></span>

[<span data-ttu-id="30b46-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="30b46-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="30b46-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="30b46-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


