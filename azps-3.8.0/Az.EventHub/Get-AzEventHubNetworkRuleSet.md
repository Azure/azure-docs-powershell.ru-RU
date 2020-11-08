---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066342"
---
# <span data-ttu-id="aff14-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="aff14-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="aff14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aff14-102">SYNOPSIS</span></span>
<span data-ttu-id="aff14-103">Получает сведения о NetworkruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="aff14-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="aff14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aff14-104">SYNTAX</span></span>

### <span data-ttu-id="aff14-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aff14-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aff14-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="aff14-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aff14-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aff14-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aff14-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aff14-108">DESCRIPTION</span></span>
<span data-ttu-id="aff14-109">Получает сведения о NetworkruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="aff14-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="aff14-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aff14-110">EXAMPLES</span></span>

### <span data-ttu-id="aff14-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aff14-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="aff14-112">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью параметров ResourceGroup и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="aff14-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="aff14-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aff14-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="aff14-114">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью пространства имен, которое находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="aff14-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="aff14-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="aff14-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="aff14-116">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью идентификатора ресурса другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff14-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="aff14-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aff14-117">PARAMETERS</span></span>

### <span data-ttu-id="aff14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff14-118">-DefaultProfile</span></span>
<span data-ttu-id="aff14-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aff14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff14-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aff14-120">-Namespace</span></span>
<span data-ttu-id="aff14-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff14-121">Namespace Name</span></span>

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

### <span data-ttu-id="aff14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff14-122">-ResourceGroupName</span></span>
<span data-ttu-id="aff14-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aff14-123">Resource Group Name</span></span>

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

### <span data-ttu-id="aff14-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aff14-124">-ResourceId</span></span>
<span data-ttu-id="aff14-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff14-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="aff14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff14-126">CommonParameters</span></span>
<span data-ttu-id="aff14-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aff14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aff14-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff14-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff14-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aff14-129">INPUTS</span></span>

### <span data-ttu-id="aff14-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aff14-130">System.String</span></span>

## <span data-ttu-id="aff14-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aff14-131">OUTPUTS</span></span>

### <span data-ttu-id="aff14-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="aff14-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="aff14-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="aff14-133">NOTES</span></span>

## <span data-ttu-id="aff14-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aff14-134">RELATED LINKS</span></span>