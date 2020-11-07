---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: 396a328de8c075b49ae4dda181158c33518eaa8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903786"
---
# <span data-ttu-id="cf46c-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cf46c-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="cf46c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf46c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf46c-103">Проверка доступности данной очереди или названия темы</span><span class="sxs-lookup"><span data-stu-id="cf46c-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="cf46c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf46c-104">SYNTAX</span></span>

### <span data-ttu-id="cf46c-105">QueueCheckNameAvailabilitySet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf46c-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf46c-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cf46c-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf46c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf46c-107">DESCRIPTION</span></span>
<span data-ttu-id="cf46c-108">Командлет **Test-AzServiceBusNameAvailability** проверяет доступность указанного имени очереди или темы</span><span class="sxs-lookup"><span data-stu-id="cf46c-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="cf46c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf46c-109">EXAMPLES</span></span>

### <span data-ttu-id="cf46c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf46c-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="cf46c-111">Возвращает значение "истина", если указанное имя $nameQueue Availabile, или возвращает значение false, если оно указано $nameQueue недоступно.</span><span class="sxs-lookup"><span data-stu-id="cf46c-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="cf46c-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cf46c-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="cf46c-113">Возвращает значение "истина", если указанное имя $nameTopic Availabile, или возвращает значение false, если оно указано $nameTopic недоступно.</span><span class="sxs-lookup"><span data-stu-id="cf46c-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="cf46c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf46c-114">PARAMETERS</span></span>

### <span data-ttu-id="cf46c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf46c-115">-DefaultProfile</span></span>
<span data-ttu-id="cf46c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf46c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf46c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf46c-117">-Name</span></span>
<span data-ttu-id="cf46c-118">Имя очереди для проверки доступности имени</span><span class="sxs-lookup"><span data-stu-id="cf46c-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cf46c-119">-Namespace</span></span>
<span data-ttu-id="cf46c-120">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="cf46c-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-121">-Очередь</span><span class="sxs-lookup"><span data-stu-id="cf46c-121">-Queue</span></span>
<span data-ttu-id="cf46c-122">Проверка доступности имени для имени очереди</span><span class="sxs-lookup"><span data-stu-id="cf46c-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf46c-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf46c-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf46c-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-125">-Темы</span><span class="sxs-lookup"><span data-stu-id="cf46c-125">-Topic</span></span>
<span data-ttu-id="cf46c-126">Проверка доступности имени для названия темы</span><span class="sxs-lookup"><span data-stu-id="cf46c-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf46c-127">CommonParameters</span></span>
<span data-ttu-id="cf46c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf46c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cf46c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf46c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf46c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf46c-130">INPUTS</span></span>

### <span data-ttu-id="cf46c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cf46c-131">System.String</span></span>

## <span data-ttu-id="cf46c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf46c-132">OUTPUTS</span></span>

### <span data-ttu-id="cf46c-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf46c-133">System.Boolean</span></span>

## <span data-ttu-id="cf46c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf46c-134">NOTES</span></span>

## <span data-ttu-id="cf46c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf46c-135">RELATED LINKS</span></span>
