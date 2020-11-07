---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28b95833e9221e5ecaa05ab33a6e2518c7cca1a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734717"
---
# <span data-ttu-id="64368-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="64368-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="64368-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64368-102">SYNOPSIS</span></span>
<span data-ttu-id="64368-103">Задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="64368-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64368-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64368-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64368-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64368-105">DESCRIPTION</span></span>
<span data-ttu-id="64368-106">Командлет **Set-AzureRmHDInsightPersistedScriptAction** задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="64368-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="64368-107">Указанное действие сценария должно быть выполнено ранее.</span><span class="sxs-lookup"><span data-stu-id="64368-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="64368-108">Действие сценария будет выполняться каждый раз при масштабировании кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="64368-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="64368-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64368-109">EXAMPLES</span></span>

### <span data-ttu-id="64368-110">Пример 1: установка ранее успешного действия сценария для сохранения или выполнение на кластере с масштабным масштабированием</span><span class="sxs-lookup"><span data-stu-id="64368-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="64368-111">Эта команда задает ранее успешное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="64368-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="64368-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64368-112">PARAMETERS</span></span>

### <span data-ttu-id="64368-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="64368-113">-ClusterName</span></span>
<span data-ttu-id="64368-114">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="64368-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="64368-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64368-115">-DefaultProfile</span></span>
<span data-ttu-id="64368-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="64368-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64368-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64368-117">-ResourceGroupName</span></span>
<span data-ttu-id="64368-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64368-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64368-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="64368-119">-ScriptExecutionId</span></span>
<span data-ttu-id="64368-120">Указывает идентификатор выполнения действия сценария, которое нужно преобразовать в материализованный.</span><span class="sxs-lookup"><span data-stu-id="64368-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="64368-121">Для повышения уровня действия сценария необходимо, чтобы оно было выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="64368-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="64368-122">Идентификатор выполнения действия сценария можно найти с помощью Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="64368-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64368-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64368-123">CommonParameters</span></span>
<span data-ttu-id="64368-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64368-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64368-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64368-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64368-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64368-126">INPUTS</span></span>

### <span data-ttu-id="64368-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="64368-127">None</span></span>
<span data-ttu-id="64368-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="64368-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64368-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64368-129">OUTPUTS</span></span>

### <span data-ttu-id="64368-130">System. void</span><span class="sxs-lookup"><span data-stu-id="64368-130">System.Void</span></span>

## <span data-ttu-id="64368-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="64368-131">NOTES</span></span>

## <span data-ttu-id="64368-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64368-132">RELATED LINKS</span></span>

[<span data-ttu-id="64368-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="64368-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="64368-134">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="64368-134">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


