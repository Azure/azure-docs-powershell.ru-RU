---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 29eab81028de58c8f23345249ef079f87380257a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730844"
---
# <span data-ttu-id="525f8-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="525f8-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="525f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="525f8-102">SYNOPSIS</span></span>
<span data-ttu-id="525f8-103">Получает сведения о NetwrokruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="525f8-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="525f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="525f8-104">SYNTAX</span></span>

### <span data-ttu-id="525f8-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="525f8-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="525f8-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="525f8-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="525f8-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="525f8-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="525f8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="525f8-108">DESCRIPTION</span></span>
<span data-ttu-id="525f8-109">Получает сведения о NetwrokruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="525f8-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="525f8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="525f8-110">EXAMPLES</span></span>

### <span data-ttu-id="525f8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="525f8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="525f8-112">Получение подробных сведений о концентраторах событий NetwrokruleSet пространства имен с помощью параметров ResourceGroup и Namesape.</span><span class="sxs-lookup"><span data-stu-id="525f8-112">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="525f8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="525f8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="525f8-114">Получение подробных сведений о концентраторах событий NetwrokruleSet пространства имен с помощью пространства имен, которое находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="525f8-114">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="525f8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="525f8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="525f8-116">Получение подробных сведений о концентраторах событий NetwrokruleSet пространства имен с помощью идентификатора ресурса другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="525f8-116">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="525f8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="525f8-117">PARAMETERS</span></span>

### <span data-ttu-id="525f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525f8-118">-DefaultProfile</span></span>
<span data-ttu-id="525f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="525f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525f8-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="525f8-120">-Namespace</span></span>
<span data-ttu-id="525f8-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="525f8-121">Namespace Name</span></span>

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

### <span data-ttu-id="525f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="525f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="525f8-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="525f8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="525f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="525f8-124">-ResourceId</span></span>
<span data-ttu-id="525f8-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="525f8-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="525f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525f8-126">CommonParameters</span></span>
<span data-ttu-id="525f8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="525f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="525f8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="525f8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525f8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="525f8-129">INPUTS</span></span>

### <span data-ttu-id="525f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="525f8-130">System.String</span></span>

## <span data-ttu-id="525f8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="525f8-131">OUTPUTS</span></span>

### <span data-ttu-id="525f8-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="525f8-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="525f8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="525f8-133">NOTES</span></span>

## <span data-ttu-id="525f8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="525f8-134">RELATED LINKS</span></span>