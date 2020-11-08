---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 56056e2933254401645a30e190a3a181b0c4514f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077742"
---
# <span data-ttu-id="a7a93-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7a93-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a7a93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7a93-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a93-103">Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="a7a93-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a7a93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7a93-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a93-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a93-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a93-106">Командлет **Get-AzHDInsightPersistedScriptAction** получает хранимые действия сценария для кластера HDInsight Azure и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="a7a93-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a7a93-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7a93-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a93-108">Пример 1: Получение сохраненных действий сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="a7a93-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a7a93-109">Эта команда получает хранимые действия сценария в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a7a93-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a7a93-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7a93-110">PARAMETERS</span></span>

### <span data-ttu-id="a7a93-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="a7a93-111">-ClusterName</span></span>
<span data-ttu-id="a7a93-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="a7a93-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a7a93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a93-113">-DefaultProfile</span></span>
<span data-ttu-id="a7a93-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7a93-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7a93-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7a93-115">-Name</span></span>
<span data-ttu-id="a7a93-116">Указывает имя сохраненного действия сценария.</span><span class="sxs-lookup"><span data-stu-id="a7a93-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a93-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7a93-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7a93-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a7a93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a93-119">CommonParameters</span></span>
<span data-ttu-id="a7a93-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7a93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a93-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a93-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a93-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7a93-122">INPUTS</span></span>

### <span data-ttu-id="a7a93-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7a93-123">None</span></span>

## <span data-ttu-id="a7a93-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a93-124">OUTPUTS</span></span>

### <span data-ttu-id="a7a93-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7a93-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="a7a93-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7a93-126">NOTES</span></span>

## <span data-ttu-id="a7a93-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7a93-127">RELATED LINKS</span></span>

[<span data-ttu-id="a7a93-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7a93-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a7a93-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7a93-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


