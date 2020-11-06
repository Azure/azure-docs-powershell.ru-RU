---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28526dd4aaa36890800a2bffd47eeae3f281d747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559812"
---
# <span data-ttu-id="efba6-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="efba6-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="efba6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efba6-102">SYNOPSIS</span></span>
<span data-ttu-id="efba6-103">Удаляет сохраненное действие сценария из кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="efba6-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efba6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efba6-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efba6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efba6-105">DESCRIPTION</span></span>
<span data-ttu-id="efba6-106">Командлет **Remove-AzureRmHDInsightPersistedScriptAction** удаляет сохраненное действие сценария из списка сохраненных действий сценария в Azure HDInsight Cluster.</span><span class="sxs-lookup"><span data-stu-id="efba6-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="efba6-107">Удаленный сценарий больше не будет выполняться при масштабировании кластера.</span><span class="sxs-lookup"><span data-stu-id="efba6-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="efba6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efba6-108">EXAMPLES</span></span>

### <span data-ttu-id="efba6-109">Пример 1: Удаление действия сценария из списка сохраненных действий сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="efba6-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="efba6-110">Эта команда удаляет действие сценария с именем Scriptaction из списка сохраненных действий сценария в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="efba6-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="efba6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efba6-111">PARAMETERS</span></span>

### <span data-ttu-id="efba6-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="efba6-112">-ClusterName</span></span>
<span data-ttu-id="efba6-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="efba6-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="efba6-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efba6-114">-Name</span></span>
<span data-ttu-id="efba6-115">Указывает имя сохраняемого сценария, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="efba6-115">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efba6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efba6-116">-ResourceGroupName</span></span>
<span data-ttu-id="efba6-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="efba6-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="efba6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efba6-118">-DefaultProfile</span></span>
<span data-ttu-id="efba6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efba6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efba6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efba6-120">CommonParameters</span></span>
<span data-ttu-id="efba6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efba6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efba6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efba6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efba6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efba6-123">INPUTS</span></span>

## <span data-ttu-id="efba6-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efba6-124">OUTPUTS</span></span>

### <span data-ttu-id="efba6-125">System. void</span><span class="sxs-lookup"><span data-stu-id="efba6-125">System.Void</span></span>

## <span data-ttu-id="efba6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="efba6-126">NOTES</span></span>

## <span data-ttu-id="efba6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efba6-127">RELATED LINKS</span></span>

[<span data-ttu-id="efba6-128">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="efba6-128">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="efba6-129">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="efba6-129">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


