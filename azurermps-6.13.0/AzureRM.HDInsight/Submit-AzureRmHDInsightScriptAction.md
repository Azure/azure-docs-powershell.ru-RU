---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 884741f6543dee05ed8236385071ad345321413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564459"
---
# <span data-ttu-id="07fc9-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="07fc9-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="07fc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="07fc9-103">Отправка нового действия сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="07fc9-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07fc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07fc9-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07fc9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="07fc9-106">Командлет **Submit-AzureRmHDInsightScriptAction** отправляет новое действие сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="07fc9-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="07fc9-107">Используйте *PersistOnSuccess* , чтобы действие сценария выполнялось каждый раз при масштабировании кластера до тех пор, пока действие сценария завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="07fc9-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="07fc9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07fc9-108">EXAMPLES</span></span>

### <span data-ttu-id="07fc9-109">Пример 1: Отправка нового действия сценария в запущенный кластер HDInsight</span><span class="sxs-lookup"><span data-stu-id="07fc9-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="07fc9-110">Эта команда отправляет действие сценария в запущенный кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="07fc9-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="07fc9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07fc9-111">PARAMETERS</span></span>

### <span data-ttu-id="07fc9-112">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="07fc9-112">-ApplicationName</span></span>
<span data-ttu-id="07fc9-113">Указывает имя приложения для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="07fc9-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="07fc9-114">Если *applicationName* задано, для *PersistOnSuccess* должно быть задано значение false, узлы должны содержать только edgenode и количество действий сценария должно равняться 1.</span><span class="sxs-lookup"><span data-stu-id="07fc9-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="07fc9-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="07fc9-115">-ClusterName</span></span>
<span data-ttu-id="07fc9-116">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="07fc9-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="07fc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fc9-117">-DefaultProfile</span></span>
<span data-ttu-id="07fc9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="07fc9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fc9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07fc9-119">-Name</span></span>
<span data-ttu-id="07fc9-120">Задает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="07fc9-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="07fc9-121">-NodeType</span><span class="sxs-lookup"><span data-stu-id="07fc9-121">-NodeTypes</span></span>
<span data-ttu-id="07fc9-122">Задает типы узлов, для которых нужно выполнить действие сценария.</span><span class="sxs-lookup"><span data-stu-id="07fc9-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="07fc9-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="07fc9-123">-Parameters</span></span>
<span data-ttu-id="07fc9-124">Задает параметры действия сценария.</span><span class="sxs-lookup"><span data-stu-id="07fc9-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="07fc9-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="07fc9-125">-PersistOnSuccess</span></span>
<span data-ttu-id="07fc9-126">Указывает на то, что действие сценария должно выполняться каждый раз при масштабировании кластера.</span><span class="sxs-lookup"><span data-stu-id="07fc9-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="07fc9-127">Этот параметр ключа игнорируется, если действие сценария завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="07fc9-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="07fc9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07fc9-128">-ResourceGroupName</span></span>
<span data-ttu-id="07fc9-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07fc9-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="07fc9-130">-URI</span><span class="sxs-lookup"><span data-stu-id="07fc9-130">-Uri</span></span>
<span data-ttu-id="07fc9-131">Задает общедоступный URI для действия сценария (сценарий PowerShell или bash).</span><span class="sxs-lookup"><span data-stu-id="07fc9-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="07fc9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fc9-132">CommonParameters</span></span>
<span data-ttu-id="07fc9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07fc9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fc9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07fc9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fc9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07fc9-135">INPUTS</span></span>

### <span data-ttu-id="07fc9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="07fc9-136">System.String</span></span>

### <span data-ttu-id="07fc9-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="07fc9-137">System.Uri</span></span>

### <span data-ttu-id="07fc9-138">Microsoft. Azure. Commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="07fc9-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="07fc9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07fc9-139">OUTPUTS</span></span>

### <span data-ttu-id="07fc9-140">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="07fc9-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="07fc9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="07fc9-141">NOTES</span></span>

## <span data-ttu-id="07fc9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07fc9-142">RELATED LINKS</span></span>

[<span data-ttu-id="07fc9-143">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="07fc9-143">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


