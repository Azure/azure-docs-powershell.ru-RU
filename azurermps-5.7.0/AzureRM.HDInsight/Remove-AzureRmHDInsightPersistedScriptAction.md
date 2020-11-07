---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 48b0fab43e104a5cae68ef26698735e89c603a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733054"
---
# <span data-ttu-id="6145d-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6145d-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="6145d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6145d-102">SYNOPSIS</span></span>
<span data-ttu-id="6145d-103">Удаляет сохраненное действие сценария из кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6145d-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6145d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6145d-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6145d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6145d-105">DESCRIPTION</span></span>
<span data-ttu-id="6145d-106">Командлет **Remove-AzureRmHDInsightPersistedScriptAction** удаляет сохраненное действие сценария из списка сохраненных действий сценария в Azure HDInsight Cluster.</span><span class="sxs-lookup"><span data-stu-id="6145d-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="6145d-107">Удаленный сценарий больше не будет выполняться при масштабировании кластера.</span><span class="sxs-lookup"><span data-stu-id="6145d-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="6145d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6145d-108">EXAMPLES</span></span>

### <span data-ttu-id="6145d-109">Пример 1: Удаление действия сценария из списка сохраненных действий сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="6145d-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="6145d-110">Эта команда удаляет действие сценария с именем Scriptaction из списка сохраненных действий сценария в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="6145d-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="6145d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6145d-111">PARAMETERS</span></span>

### <span data-ttu-id="6145d-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="6145d-112">-ClusterName</span></span>
<span data-ttu-id="6145d-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6145d-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6145d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6145d-114">-DefaultProfile</span></span>
<span data-ttu-id="6145d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6145d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6145d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6145d-116">-Name</span></span>
<span data-ttu-id="6145d-117">Указывает имя сохраняемого сценария, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6145d-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6145d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6145d-118">-ResourceGroupName</span></span>
<span data-ttu-id="6145d-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6145d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6145d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6145d-120">CommonParameters</span></span>
<span data-ttu-id="6145d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6145d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6145d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6145d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6145d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6145d-123">INPUTS</span></span>

### <span data-ttu-id="6145d-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="6145d-124">None</span></span>
<span data-ttu-id="6145d-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6145d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6145d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6145d-126">OUTPUTS</span></span>

### <span data-ttu-id="6145d-127">System. void</span><span class="sxs-lookup"><span data-stu-id="6145d-127">System.Void</span></span>

## <span data-ttu-id="6145d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6145d-128">NOTES</span></span>

## <span data-ttu-id="6145d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6145d-129">RELATED LINKS</span></span>

[<span data-ttu-id="6145d-130">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6145d-130">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="6145d-131">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6145d-131">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


