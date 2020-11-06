---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566727"
---
# <span data-ttu-id="38661-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="38661-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="38661-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38661-102">SYNOPSIS</span></span>
<span data-ttu-id="38661-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="38661-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38661-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38661-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="38661-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38661-105">DESCRIPTION</span></span>
<span data-ttu-id="38661-106">Командлет Remove-AzureRmEventHubNamespace удаляет и удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="38661-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="38661-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38661-107">EXAMPLES</span></span>

### <span data-ttu-id="38661-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38661-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="38661-109">Удаляет пространство имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="38661-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="38661-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38661-110">PARAMETERS</span></span>

### <span data-ttu-id="38661-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38661-111">-ResourceGroupName</span></span>
<span data-ttu-id="38661-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38661-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38661-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38661-113">-Confirm</span></span>
<span data-ttu-id="38661-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38661-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38661-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38661-115">-WhatIf</span></span>
<span data-ttu-id="38661-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38661-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38661-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38661-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38661-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38661-118">-Name</span></span>
<span data-ttu-id="38661-119">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="38661-119">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="38661-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38661-120">INPUTS</span></span>

### <span data-ttu-id="38661-121">System. String</span><span class="sxs-lookup"><span data-stu-id="38661-121">System.String</span></span>

## <span data-ttu-id="38661-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38661-122">OUTPUTS</span></span>

### <span data-ttu-id="38661-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="38661-123">System.Object</span></span>

## <span data-ttu-id="38661-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="38661-124">NOTES</span></span>

## <span data-ttu-id="38661-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38661-125">RELATED LINKS</span></span>

