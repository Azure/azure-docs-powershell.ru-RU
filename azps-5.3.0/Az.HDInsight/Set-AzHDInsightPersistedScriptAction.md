---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: f593989125642d03a9dff1b48bbc7430498b2a36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506290"
---
# <span data-ttu-id="b4f70-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b4f70-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="b4f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4f70-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f70-103">Для ранее выполненного действия сценария устанавливается его сохраняемая возможность.</span><span class="sxs-lookup"><span data-stu-id="b4f70-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="b4f70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4f70-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4f70-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4f70-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f70-106">Для выполнения ранее выполненного действия сценария задана возможность сохраняемого действия сценария **Set-AzHDInsightPersistedScriptAction.**</span><span class="sxs-lookup"><span data-stu-id="b4f70-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="b4f70-107">Указанное действие сценария должно быть ранее успешным.</span><span class="sxs-lookup"><span data-stu-id="b4f70-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="b4f70-108">Сценарий будет запускаться при каждом масштабе кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4f70-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="b4f70-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4f70-109">EXAMPLES</span></span>

### <span data-ttu-id="b4f70-110">Пример 1. Настройка сохраняемого ранее успешного действия сценария или масштабирования кластеров</span><span class="sxs-lookup"><span data-stu-id="b4f70-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="b4f70-111">Эта команда задает для ранее успешного действия сценария сохраняется действие сценария.</span><span class="sxs-lookup"><span data-stu-id="b4f70-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="b4f70-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4f70-112">PARAMETERS</span></span>

### <span data-ttu-id="b4f70-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b4f70-113">-ClusterName</span></span>
<span data-ttu-id="b4f70-114">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="b4f70-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b4f70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f70-115">-DefaultProfile</span></span>
<span data-ttu-id="b4f70-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4f70-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4f70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f70-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4f70-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4f70-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b4f70-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="b4f70-119">-ScriptExecutionId</span></span>
<span data-ttu-id="b4f70-120">Определяет ИД выполнения действия сценария, который нужно повысить до сохраняемого.</span><span class="sxs-lookup"><span data-stu-id="b4f70-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="b4f70-121">Для продвижения этого действия сценарию необходимо, чтобы его можно было продвигать.</span><span class="sxs-lookup"><span data-stu-id="b4f70-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="b4f70-122">Вы можете найти ИД выполнения сценария с помощью Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="b4f70-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4f70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f70-123">CommonParameters</span></span>
<span data-ttu-id="b4f70-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f70-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4f70-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f70-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4f70-126">INPUTS</span></span>

### <span data-ttu-id="b4f70-127">Нет</span><span class="sxs-lookup"><span data-stu-id="b4f70-127">None</span></span>

## <span data-ttu-id="b4f70-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4f70-128">OUTPUTS</span></span>

### <span data-ttu-id="b4f70-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="b4f70-129">System.Void</span></span>

## <span data-ttu-id="b4f70-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4f70-130">NOTES</span></span>

## <span data-ttu-id="b4f70-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4f70-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4f70-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b4f70-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="b4f70-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b4f70-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


