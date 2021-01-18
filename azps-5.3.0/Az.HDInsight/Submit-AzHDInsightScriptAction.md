---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 3cbd73075445bdcf65efafb266476c522dc4b1ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507282"
---
# <span data-ttu-id="f34ef-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="f34ef-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="f34ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f34ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f34ef-103">Отправка нового действия сценария в кластер Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f34ef-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f34ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f34ef-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f34ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f34ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f34ef-106">Cmdlet **Submit-AzHDInsightScriptAction** передает новое действие сценария в кластер Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f34ef-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="f34ef-107">Используйте *PersistOnSuccess,* чтобы действие сценария запускалось при каждом масштабе кластера, если изначально это действие было успешным.</span><span class="sxs-lookup"><span data-stu-id="f34ef-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="f34ef-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f34ef-108">EXAMPLES</span></span>

### <span data-ttu-id="f34ef-109">Пример 1. Отправка нового действия сценария в работающий кластер HDInsight</span><span class="sxs-lookup"><span data-stu-id="f34ef-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="f34ef-110">Эта команда передает действие сценария в работающий кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f34ef-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="f34ef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f34ef-111">PARAMETERS</span></span>

### <span data-ttu-id="f34ef-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f34ef-112">-ApplicationName</span></span>
<span data-ttu-id="f34ef-113">Указывает имя приложения для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="f34ef-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="f34ef-114">Если *задано* имя приложения, *persistOnSuccess* должно иметь значение False, узлы должны содержать только edgenode, а количество действий сценария должно равняться 1.</span><span class="sxs-lookup"><span data-stu-id="f34ef-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34ef-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f34ef-115">-ClusterName</span></span>
<span data-ttu-id="f34ef-116">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="f34ef-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f34ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34ef-117">-DefaultProfile</span></span>
<span data-ttu-id="f34ef-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f34ef-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f34ef-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f34ef-119">-Name</span></span>
<span data-ttu-id="f34ef-120">Указывает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="f34ef-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34ef-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="f34ef-121">-NodeTypes</span></span>
<span data-ttu-id="f34ef-122">Указывает типы узлов, к которым нужно выполнить действие сценария.</span><span class="sxs-lookup"><span data-stu-id="f34ef-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34ef-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="f34ef-123">-Parameters</span></span>
<span data-ttu-id="f34ef-124">Определяет параметры для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="f34ef-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34ef-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="f34ef-125">-PersistOnSuccess</span></span>
<span data-ttu-id="f34ef-126">Указывает на то, что действие сценария должно запускаться при каждом масштабе кластера.</span><span class="sxs-lookup"><span data-stu-id="f34ef-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="f34ef-127">Этот параметр переключателя игнорируется, если действие сценария изначально не работает.</span><span class="sxs-lookup"><span data-stu-id="f34ef-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f34ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f34ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="f34ef-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f34ef-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f34ef-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="f34ef-130">-Uri</span></span>
<span data-ttu-id="f34ef-131">Указывает общедоступный URI для действия сценария (сценарий PowerShell или Bash).</span><span class="sxs-lookup"><span data-stu-id="f34ef-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34ef-132">CommonParameters</span></span>
<span data-ttu-id="f34ef-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f34ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34ef-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f34ef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34ef-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f34ef-135">INPUTS</span></span>

### <span data-ttu-id="f34ef-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f34ef-136">System.String</span></span>

### <span data-ttu-id="f34ef-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="f34ef-137">System.Uri</span></span>

### <span data-ttu-id="f34ef-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="f34ef-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="f34ef-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f34ef-139">OUTPUTS</span></span>

### <span data-ttu-id="f34ef-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="f34ef-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="f34ef-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f34ef-141">NOTES</span></span>

## <span data-ttu-id="f34ef-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f34ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="f34ef-143">Add-AzhdInsightScriptaction</span><span class="sxs-lookup"><span data-stu-id="f34ef-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


