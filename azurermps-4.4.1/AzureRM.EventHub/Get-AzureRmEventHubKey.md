---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569495"
---
# <span data-ttu-id="27b24-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="27b24-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="27b24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27b24-102">SYNOPSIS</span></span>
<span data-ttu-id="27b24-103">Возвращает сведения о первичном ключе для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="27b24-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27b24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27b24-104">SYNTAX</span></span>

### <span data-ttu-id="27b24-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27b24-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="27b24-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="27b24-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="27b24-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27b24-107">DESCRIPTION</span></span>
<span data-ttu-id="27b24-108">Командлет Get-AzureRmEventHubKey возвращает первичные и вторичные connectionStrings и сведения о ключах для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="27b24-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="27b24-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27b24-109">EXAMPLES</span></span>

### <span data-ttu-id="27b24-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27b24-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="27b24-111">Получение подробных сведений о первичных и вспомогательных элементах ConnectionString и ключах для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="27b24-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="27b24-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27b24-112">PARAMETERS</span></span>

### <span data-ttu-id="27b24-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b24-113">-ResourceGroupName</span></span>
<span data-ttu-id="27b24-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27b24-114">Resource group name.</span></span>

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

### <span data-ttu-id="27b24-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="27b24-115">-EventHub</span></span>
<span data-ttu-id="27b24-116">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="27b24-116">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b24-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27b24-117">-Name</span></span>
<span data-ttu-id="27b24-118">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="27b24-118">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b24-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27b24-119">-Namespace</span></span>
<span data-ttu-id="27b24-120">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="27b24-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="27b24-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27b24-121">INPUTS</span></span>

### <span data-ttu-id="27b24-122">System. String</span><span class="sxs-lookup"><span data-stu-id="27b24-122">System.String</span></span>

## <span data-ttu-id="27b24-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27b24-123">OUTPUTS</span></span>

### <span data-ttu-id="27b24-124">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="27b24-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="27b24-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="27b24-125">NOTES</span></span>

## <span data-ttu-id="27b24-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27b24-126">RELATED LINKS</span></span>

