---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 64dae906f7f28e119d8550ecf5bb31d1b6ca7b27
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910397"
---
# <span data-ttu-id="e1adc-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1adc-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="e1adc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1adc-102">SYNOPSIS</span></span>
<span data-ttu-id="e1adc-103">Получает сведения о NetworkruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="e1adc-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="e1adc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1adc-104">SYNTAX</span></span>

### <span data-ttu-id="e1adc-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1adc-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1adc-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e1adc-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1adc-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1adc-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1adc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1adc-108">DESCRIPTION</span></span>
<span data-ttu-id="e1adc-109">Получает сведения о NetworkruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="e1adc-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="e1adc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1adc-110">EXAMPLES</span></span>

### <span data-ttu-id="e1adc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1adc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="e1adc-112">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью параметров ResourceGroup и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e1adc-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="e1adc-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e1adc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="e1adc-114">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью пространства имен, которое находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="e1adc-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="e1adc-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e1adc-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="e1adc-116">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью идентификатора ресурса другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="e1adc-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="e1adc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1adc-117">PARAMETERS</span></span>

### <span data-ttu-id="e1adc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1adc-118">-DefaultProfile</span></span>
<span data-ttu-id="e1adc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1adc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1adc-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e1adc-120">-Namespace</span></span>
<span data-ttu-id="e1adc-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e1adc-121">Namespace Name</span></span>

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

### <span data-ttu-id="e1adc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1adc-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1adc-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e1adc-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e1adc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1adc-124">-ResourceId</span></span>
<span data-ttu-id="e1adc-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="e1adc-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="e1adc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1adc-126">CommonParameters</span></span>
<span data-ttu-id="e1adc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1adc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e1adc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1adc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1adc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1adc-129">INPUTS</span></span>

### <span data-ttu-id="e1adc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e1adc-130">System.String</span></span>

## <span data-ttu-id="e1adc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1adc-131">OUTPUTS</span></span>

### <span data-ttu-id="e1adc-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="e1adc-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="e1adc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1adc-133">NOTES</span></span>

## <span data-ttu-id="e1adc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1adc-134">RELATED LINKS</span></span>