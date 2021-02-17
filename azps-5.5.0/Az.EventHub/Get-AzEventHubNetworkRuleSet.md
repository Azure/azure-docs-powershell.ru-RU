---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220001"
---
# <span data-ttu-id="05e2f-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="05e2f-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="05e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="05e2f-103">Получает сведения о NetworkruleSet NetworkruleSet концентратора событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="05e2f-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="05e2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05e2f-104">SYNTAX</span></span>

### <span data-ttu-id="05e2f-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05e2f-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e2f-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="05e2f-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e2f-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e2f-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05e2f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05e2f-108">DESCRIPTION</span></span>
<span data-ttu-id="05e2f-109">Получает сведения о NetworkruleSet NetworkruleSet концентратора событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="05e2f-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="05e2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05e2f-110">EXAMPLES</span></span>

### <span data-ttu-id="05e2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05e2f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="05e2f-112">Получите сведения о NetworkruleSet NetworkruleSet пространства имен с помощью параметров ResourceGroup и Namespace.</span><span class="sxs-lookup"><span data-stu-id="05e2f-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="05e2f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="05e2f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="05e2f-114">Получите сведения о NetworkruleSet NetworkruleSet событий с помощью пространства имен, которая находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="05e2f-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="05e2f-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="05e2f-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="05e2f-116">Получить сведения о NetworkruleSet Концентраторов событий пространства имен с помощью ИД ресурса из другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="05e2f-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="05e2f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05e2f-117">PARAMETERS</span></span>

### <span data-ttu-id="05e2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e2f-118">-DefaultProfile</span></span>
<span data-ttu-id="05e2f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05e2f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05e2f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="05e2f-120">-Namespace</span></span>
<span data-ttu-id="05e2f-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="05e2f-121">Namespace Name</span></span>

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

### <span data-ttu-id="05e2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="05e2f-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="05e2f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="05e2f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05e2f-124">-ResourceId</span></span>
<span data-ttu-id="05e2f-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="05e2f-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="05e2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e2f-126">CommonParameters</span></span>
<span data-ttu-id="05e2f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="05e2f-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e2f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e2f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05e2f-129">INPUTS</span></span>

### <span data-ttu-id="05e2f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="05e2f-130">System.String</span></span>

## <span data-ttu-id="05e2f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05e2f-131">OUTPUTS</span></span>

### <span data-ttu-id="05e2f-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="05e2f-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="05e2f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05e2f-133">NOTES</span></span>

## <span data-ttu-id="05e2f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05e2f-134">RELATED LINKS</span></span>