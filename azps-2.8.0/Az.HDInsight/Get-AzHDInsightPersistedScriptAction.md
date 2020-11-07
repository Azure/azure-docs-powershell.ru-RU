---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a437c27aaa5caea7ae0efb7ab477fe643a5c80a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720835"
---
# <span data-ttu-id="3cfed-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3cfed-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="3cfed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cfed-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfed-103">Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="3cfed-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="3cfed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cfed-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cfed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cfed-105">DESCRIPTION</span></span>
<span data-ttu-id="3cfed-106">Командлет **Get-AzHDInsightPersistedScriptAction** получает хранимые действия сценария для кластера HDInsight Azure и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="3cfed-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="3cfed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cfed-107">EXAMPLES</span></span>

### <span data-ttu-id="3cfed-108">Пример 1: Получение сохраненных действий сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="3cfed-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="3cfed-109">Эта команда получает хранимые действия сценария в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="3cfed-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3cfed-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cfed-110">PARAMETERS</span></span>

### <span data-ttu-id="3cfed-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="3cfed-111">-ClusterName</span></span>
<span data-ttu-id="3cfed-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="3cfed-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3cfed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfed-113">-DefaultProfile</span></span>
<span data-ttu-id="3cfed-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3cfed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cfed-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3cfed-115">-Name</span></span>
<span data-ttu-id="3cfed-116">Указывает имя сохраненного действия сценария.</span><span class="sxs-lookup"><span data-stu-id="3cfed-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="3cfed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cfed-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cfed-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cfed-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3cfed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfed-119">CommonParameters</span></span>
<span data-ttu-id="3cfed-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cfed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfed-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cfed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfed-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cfed-122">INPUTS</span></span>

### <span data-ttu-id="3cfed-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3cfed-123">None</span></span>

## <span data-ttu-id="3cfed-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cfed-124">OUTPUTS</span></span>

### <span data-ttu-id="3cfed-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="3cfed-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="3cfed-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cfed-126">NOTES</span></span>

## <span data-ttu-id="3cfed-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cfed-127">RELATED LINKS</span></span>

[<span data-ttu-id="3cfed-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3cfed-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="3cfed-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3cfed-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


