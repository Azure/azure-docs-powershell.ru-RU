---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 5c2eb27ff2da4ac97cc2e7ec77e1ef67e0db3784
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900437"
---
# <span data-ttu-id="b9af8-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b9af8-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="b9af8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9af8-102">SYNOPSIS</span></span>
<span data-ttu-id="b9af8-103">Задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="b9af8-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="b9af8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9af8-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9af8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9af8-105">DESCRIPTION</span></span>
<span data-ttu-id="b9af8-106">Командлет **Set-AzHDInsightPersistedScriptAction** задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="b9af8-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="b9af8-107">Указанное действие сценария должно быть выполнено ранее.</span><span class="sxs-lookup"><span data-stu-id="b9af8-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="b9af8-108">Действие сценария будет выполняться каждый раз при масштабировании кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="b9af8-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="b9af8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9af8-109">EXAMPLES</span></span>

### <span data-ttu-id="b9af8-110">Пример 1: установка ранее успешного действия сценария для сохранения или выполнение на кластере с масштабным масштабированием</span><span class="sxs-lookup"><span data-stu-id="b9af8-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="b9af8-111">Эта команда задает ранее успешное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="b9af8-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="b9af8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9af8-112">PARAMETERS</span></span>

### <span data-ttu-id="b9af8-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b9af8-113">-ClusterName</span></span>
<span data-ttu-id="b9af8-114">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b9af8-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b9af8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9af8-115">-DefaultProfile</span></span>
<span data-ttu-id="b9af8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9af8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9af8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9af8-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9af8-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9af8-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b9af8-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="b9af8-119">-ScriptExecutionId</span></span>
<span data-ttu-id="b9af8-120">Указывает идентификатор выполнения действия сценария, которое нужно преобразовать в материализованный.</span><span class="sxs-lookup"><span data-stu-id="b9af8-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="b9af8-121">Для повышения уровня действия сценария необходимо, чтобы оно было выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="b9af8-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="b9af8-122">Идентификатор выполнения действия сценария можно найти с помощью Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="b9af8-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="b9af8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9af8-123">CommonParameters</span></span>
<span data-ttu-id="b9af8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9af8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9af8-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9af8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9af8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9af8-126">INPUTS</span></span>

### <span data-ttu-id="b9af8-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9af8-127">None</span></span>

## <span data-ttu-id="b9af8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9af8-128">OUTPUTS</span></span>

### <span data-ttu-id="b9af8-129">System. void</span><span class="sxs-lookup"><span data-stu-id="b9af8-129">System.Void</span></span>

## <span data-ttu-id="b9af8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9af8-130">NOTES</span></span>

## <span data-ttu-id="b9af8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9af8-131">RELATED LINKS</span></span>

[<span data-ttu-id="b9af8-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b9af8-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="b9af8-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b9af8-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


