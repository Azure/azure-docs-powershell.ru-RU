---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568067"
---
# <span data-ttu-id="dc63d-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="dc63d-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="dc63d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc63d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc63d-103">Получает сведения о пространстве имен концентраторов событий или получает список всех пространств имен концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="dc63d-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc63d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc63d-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="dc63d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc63d-105">DESCRIPTION</span></span>
<span data-ttu-id="dc63d-106">Командлет Get-AzureRmEventHubNamespace получает либо сведения о заданном пространстве имен концентраторов событий, либо список всех пространств имен концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="dc63d-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="dc63d-107">Если указано имя пространства имен, возвращается информация об одном пространстве имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="dc63d-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="dc63d-108">Если имя пространства имен не указано, возвращается список пространств имен.</span><span class="sxs-lookup"><span data-stu-id="dc63d-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="dc63d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc63d-109">EXAMPLES</span></span>

### <span data-ttu-id="dc63d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc63d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="dc63d-111">Получает сведения о пространстве имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="dc63d-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="dc63d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc63d-112">PARAMETERS</span></span>

### <span data-ttu-id="dc63d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc63d-113">-ResourceGroupName</span></span>
<span data-ttu-id="dc63d-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc63d-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc63d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc63d-115">-Name</span></span>
<span data-ttu-id="dc63d-116">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="dc63d-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="dc63d-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc63d-117">INPUTS</span></span>

### <span data-ttu-id="dc63d-118">System. String</span><span class="sxs-lookup"><span data-stu-id="dc63d-118">System.String</span></span>

## <span data-ttu-id="dc63d-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc63d-119">OUTPUTS</span></span>

### <span data-ttu-id="dc63d-120">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.0.1.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="dc63d-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc63d-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc63d-121">NOTES</span></span>

## <span data-ttu-id="dc63d-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc63d-122">RELATED LINKS</span></span>

