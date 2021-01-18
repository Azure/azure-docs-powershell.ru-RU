---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507506"
---
# <span data-ttu-id="8ba78-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ba78-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="8ba78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba78-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba78-103">Получает сведения о NetworkruleSet NetworkruleSet концентратора событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba78-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8ba78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ba78-104">SYNTAX</span></span>

### <span data-ttu-id="8ba78-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ba78-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ba78-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8ba78-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ba78-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba78-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ba78-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ba78-108">DESCRIPTION</span></span>
<span data-ttu-id="8ba78-109">Получает сведения о NetworkruleSet NetworkruleSet концентратора событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba78-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8ba78-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ba78-110">EXAMPLES</span></span>

### <span data-ttu-id="8ba78-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ba78-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="8ba78-112">Получите сведения о NetworkruleSet NetworkruleSet пространства имен с помощью параметров ResourceGroup и Namespace.</span><span class="sxs-lookup"><span data-stu-id="8ba78-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="8ba78-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8ba78-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="8ba78-114">Получите сведения о NetworkruleSet NetworkruleSet событий с помощью пространства имен, которая находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8ba78-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="8ba78-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8ba78-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="8ba78-116">Получить сведения о NetworkruleSet Концентраторов событий пространства имен с помощью ИД ресурса из другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="8ba78-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="8ba78-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ba78-117">PARAMETERS</span></span>

### <span data-ttu-id="8ba78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba78-118">-DefaultProfile</span></span>
<span data-ttu-id="8ba78-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba78-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba78-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ba78-120">-Namespace</span></span>
<span data-ttu-id="8ba78-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="8ba78-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba78-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ba78-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8ba78-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba78-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ba78-124">-ResourceId</span></span>
<span data-ttu-id="8ba78-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="8ba78-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba78-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba78-126">CommonParameters</span></span>
<span data-ttu-id="8ba78-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba78-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8ba78-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba78-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba78-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ba78-129">INPUTS</span></span>

### <span data-ttu-id="8ba78-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8ba78-130">System.String</span></span>

## <span data-ttu-id="8ba78-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ba78-131">OUTPUTS</span></span>

### <span data-ttu-id="8ba78-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8ba78-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8ba78-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ba78-133">NOTES</span></span>

## <span data-ttu-id="8ba78-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ba78-134">RELATED LINKS</span></span>