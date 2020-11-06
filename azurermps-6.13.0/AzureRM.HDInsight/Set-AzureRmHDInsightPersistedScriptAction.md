---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 07f501be4ac775a9d80c43173e13fccf3057cc26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560183"
---
# <span data-ttu-id="aaca0-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="aaca0-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="aaca0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaca0-102">SYNOPSIS</span></span>
<span data-ttu-id="aaca0-103">Задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="aaca0-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaca0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaca0-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaca0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaca0-105">DESCRIPTION</span></span>
<span data-ttu-id="aaca0-106">Командлет **Set-AzureRmHDInsightPersistedScriptAction** задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="aaca0-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="aaca0-107">Указанное действие сценария должно быть выполнено ранее.</span><span class="sxs-lookup"><span data-stu-id="aaca0-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="aaca0-108">Действие сценария будет выполняться каждый раз при масштабировании кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="aaca0-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="aaca0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaca0-109">EXAMPLES</span></span>

### <span data-ttu-id="aaca0-110">Пример 1: установка ранее успешного действия сценария для сохранения или выполнение на кластере с масштабным масштабированием</span><span class="sxs-lookup"><span data-stu-id="aaca0-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="aaca0-111">Эта команда задает ранее успешное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="aaca0-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="aaca0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaca0-112">PARAMETERS</span></span>

### <span data-ttu-id="aaca0-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="aaca0-113">-ClusterName</span></span>
<span data-ttu-id="aaca0-114">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="aaca0-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="aaca0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaca0-115">-DefaultProfile</span></span>
<span data-ttu-id="aaca0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aaca0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaca0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaca0-117">-ResourceGroupName</span></span>
<span data-ttu-id="aaca0-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaca0-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aaca0-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="aaca0-119">-ScriptExecutionId</span></span>
<span data-ttu-id="aaca0-120">Указывает идентификатор выполнения действия сценария, которое нужно преобразовать в материализованный.</span><span class="sxs-lookup"><span data-stu-id="aaca0-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="aaca0-121">Для повышения уровня действия сценария необходимо, чтобы оно было выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="aaca0-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="aaca0-122">Идентификатор выполнения действия сценария можно найти с помощью Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="aaca0-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="aaca0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaca0-123">CommonParameters</span></span>
<span data-ttu-id="aaca0-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaca0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaca0-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaca0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaca0-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaca0-126">INPUTS</span></span>

### <span data-ttu-id="aaca0-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="aaca0-127">None</span></span>

## <span data-ttu-id="aaca0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaca0-128">OUTPUTS</span></span>

### <span data-ttu-id="aaca0-129">System. void</span><span class="sxs-lookup"><span data-stu-id="aaca0-129">System.Void</span></span>

## <span data-ttu-id="aaca0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaca0-130">NOTES</span></span>

## <span data-ttu-id="aaca0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaca0-131">RELATED LINKS</span></span>

[<span data-ttu-id="aaca0-132">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="aaca0-132">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="aaca0-133">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="aaca0-133">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


