---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569484"
---
# <span data-ttu-id="c42a0-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="c42a0-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="c42a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c42a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c42a0-103">Получает сведения о первичных, вспомогательных элементах ConnectionString и ключах для правила авторизации указанного правила авторизации пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="c42a0-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c42a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c42a0-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="c42a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c42a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c42a0-106">Командлет Get-AzureRmEventHubNamespaceKey возвращает основные и дополнительные сведения о заданных правилах авторизации в заданном пространстве имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="c42a0-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="c42a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c42a0-107">EXAMPLES</span></span>

### <span data-ttu-id="c42a0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c42a0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="c42a0-109">Получает сведения о первичных и вторичных адресах ConnectionString и ключах для правила авторизации \` MyAuthRuleName в \` пространстве имен \` MyNamespaceName \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c42a0-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c42a0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c42a0-110">PARAMETERS</span></span>

### <span data-ttu-id="c42a0-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c42a0-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="c42a0-112">Имя правила авторизации в пространстве имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="c42a0-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42a0-113">-+ +</span><span class="sxs-lookup"><span data-stu-id="c42a0-113">-NamespaceName</span></span>
<span data-ttu-id="c42a0-114">Имя пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="c42a0-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42a0-115">-ResourceGroupName</span></span>
<span data-ttu-id="c42a0-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c42a0-116">Resource group name.</span></span>

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

## <span data-ttu-id="c42a0-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c42a0-117">INPUTS</span></span>

### <span data-ttu-id="c42a0-118">System. String</span><span class="sxs-lookup"><span data-stu-id="c42a0-118">System.String</span></span>

## <span data-ttu-id="c42a0-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c42a0-119">OUTPUTS</span></span>

### <span data-ttu-id="c42a0-120">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c42a0-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="c42a0-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="c42a0-121">NOTES</span></span>

## <span data-ttu-id="c42a0-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c42a0-122">RELATED LINKS</span></span>

