---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: dfae83e6bd540a83475f02ed95382bebff2ec7a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236688"
---
# <span data-ttu-id="70aba-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="70aba-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="70aba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70aba-102">SYNOPSIS</span></span>
<span data-ttu-id="70aba-103">Отправка нового действия сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="70aba-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70aba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70aba-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70aba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70aba-105">DESCRIPTION</span></span>
<span data-ttu-id="70aba-106">Командлет **Submit-AzHDInsightScriptAction** отправляет новое действие сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="70aba-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="70aba-107">Используйте *PersistOnSuccess* , чтобы действие сценария выполнялось каждый раз при масштабировании кластера до тех пор, пока действие сценария завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="70aba-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="70aba-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70aba-108">EXAMPLES</span></span>

### <span data-ttu-id="70aba-109">Пример 1: Отправка нового действия сценария в запущенный кластер HDInsight</span><span class="sxs-lookup"><span data-stu-id="70aba-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="70aba-110">Эта команда отправляет действие сценария в запущенный кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70aba-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="70aba-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70aba-111">PARAMETERS</span></span>

### <span data-ttu-id="70aba-112">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="70aba-112">-ApplicationName</span></span>
<span data-ttu-id="70aba-113">Указывает имя приложения для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="70aba-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="70aba-114">Если *applicationName* задано, для *PersistOnSuccess* должно быть задано значение false, узлы должны содержать только edgenode и количество действий сценария должно равняться 1.</span><span class="sxs-lookup"><span data-stu-id="70aba-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="70aba-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="70aba-115">-ClusterName</span></span>
<span data-ttu-id="70aba-116">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="70aba-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="70aba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70aba-117">-DefaultProfile</span></span>
<span data-ttu-id="70aba-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="70aba-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70aba-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70aba-119">-Name</span></span>
<span data-ttu-id="70aba-120">Задает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="70aba-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="70aba-121">-NodeType</span><span class="sxs-lookup"><span data-stu-id="70aba-121">-NodeTypes</span></span>
<span data-ttu-id="70aba-122">Задает типы узлов, для которых нужно выполнить действие сценария.</span><span class="sxs-lookup"><span data-stu-id="70aba-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="70aba-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="70aba-123">-Parameters</span></span>
<span data-ttu-id="70aba-124">Задает параметры действия сценария.</span><span class="sxs-lookup"><span data-stu-id="70aba-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="70aba-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="70aba-125">-PersistOnSuccess</span></span>
<span data-ttu-id="70aba-126">Указывает на то, что действие сценария должно выполняться каждый раз при масштабировании кластера.</span><span class="sxs-lookup"><span data-stu-id="70aba-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="70aba-127">Этот параметр ключа игнорируется, если действие сценария завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="70aba-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="70aba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70aba-128">-ResourceGroupName</span></span>
<span data-ttu-id="70aba-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70aba-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="70aba-130">-URI</span><span class="sxs-lookup"><span data-stu-id="70aba-130">-Uri</span></span>
<span data-ttu-id="70aba-131">Задает общедоступный URI для действия сценария (сценарий PowerShell или bash).</span><span class="sxs-lookup"><span data-stu-id="70aba-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="70aba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70aba-132">CommonParameters</span></span>
<span data-ttu-id="70aba-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70aba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70aba-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70aba-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70aba-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70aba-135">INPUTS</span></span>

### <span data-ttu-id="70aba-136">System. String</span><span class="sxs-lookup"><span data-stu-id="70aba-136">System.String</span></span>

### <span data-ttu-id="70aba-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="70aba-137">System.Uri</span></span>

### <span data-ttu-id="70aba-138">Microsoft. Azure. Commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="70aba-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="70aba-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70aba-139">OUTPUTS</span></span>

### <span data-ttu-id="70aba-140">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="70aba-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="70aba-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="70aba-141">NOTES</span></span>

## <span data-ttu-id="70aba-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70aba-142">RELATED LINKS</span></span>

[<span data-ttu-id="70aba-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="70aba-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


