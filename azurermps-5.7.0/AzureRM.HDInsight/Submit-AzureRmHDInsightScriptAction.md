---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569032"
---
# <span data-ttu-id="16bdf-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="16bdf-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="16bdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="16bdf-103">Отправка нового действия сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="16bdf-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16bdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16bdf-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16bdf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="16bdf-106">Командлет **Submit-AzureRmHDInsightScriptAction** отправляет новое действие сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="16bdf-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="16bdf-107">Используйте *PersistOnSuccess* , чтобы действие сценария выполнялось каждый раз при масштабировании кластера до тех пор, пока действие сценария завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="16bdf-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="16bdf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16bdf-108">EXAMPLES</span></span>

### <span data-ttu-id="16bdf-109">Пример 1: Отправка нового действия сценария в запущенный кластер HDInsight</span><span class="sxs-lookup"><span data-stu-id="16bdf-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="16bdf-110">Эта команда отправляет действие сценария в запущенный кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="16bdf-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="16bdf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16bdf-111">PARAMETERS</span></span>

### <span data-ttu-id="16bdf-112">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="16bdf-112">-ApplicationName</span></span>
<span data-ttu-id="16bdf-113">Указывает имя приложения для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="16bdf-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="16bdf-114">Если *applicationName* задано, для *PersistOnSuccess* должно быть задано значение false, узлы должны содержать только edgenode и количество действий сценария должно равняться 1.</span><span class="sxs-lookup"><span data-stu-id="16bdf-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bdf-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="16bdf-115">-ClusterName</span></span>
<span data-ttu-id="16bdf-116">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="16bdf-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="16bdf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bdf-117">-DefaultProfile</span></span>
<span data-ttu-id="16bdf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16bdf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16bdf-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16bdf-119">-Name</span></span>
<span data-ttu-id="16bdf-120">Задает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="16bdf-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bdf-121">-NodeType</span><span class="sxs-lookup"><span data-stu-id="16bdf-121">-NodeTypes</span></span>
<span data-ttu-id="16bdf-122">Задает типы узлов, для которых нужно выполнить действие сценария.</span><span class="sxs-lookup"><span data-stu-id="16bdf-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bdf-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="16bdf-123">-Parameters</span></span>
<span data-ttu-id="16bdf-124">Задает параметры действия сценария.</span><span class="sxs-lookup"><span data-stu-id="16bdf-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bdf-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="16bdf-125">-PersistOnSuccess</span></span>
<span data-ttu-id="16bdf-126">Указывает на то, что действие сценария должно выполняться каждый раз при масштабировании кластера.</span><span class="sxs-lookup"><span data-stu-id="16bdf-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="16bdf-127">Этот параметр ключа игнорируется, если действие сценария завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="16bdf-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bdf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16bdf-128">-ResourceGroupName</span></span>
<span data-ttu-id="16bdf-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16bdf-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="16bdf-130">-URI</span><span class="sxs-lookup"><span data-stu-id="16bdf-130">-Uri</span></span>
<span data-ttu-id="16bdf-131">Задает общедоступный URI для действия сценария (сценарий PowerShell или bash).</span><span class="sxs-lookup"><span data-stu-id="16bdf-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bdf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bdf-132">CommonParameters</span></span>
<span data-ttu-id="16bdf-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16bdf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bdf-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16bdf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bdf-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16bdf-135">INPUTS</span></span>

### <span data-ttu-id="16bdf-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="16bdf-136">None</span></span>
<span data-ttu-id="16bdf-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="16bdf-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16bdf-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16bdf-138">OUTPUTS</span></span>

### <span data-ttu-id="16bdf-139">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="16bdf-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="16bdf-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="16bdf-140">NOTES</span></span>

## <span data-ttu-id="16bdf-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16bdf-141">RELATED LINKS</span></span>

[<span data-ttu-id="16bdf-142">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="16bdf-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


