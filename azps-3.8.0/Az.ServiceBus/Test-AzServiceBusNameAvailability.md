---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065352"
---
# <span data-ttu-id="ffe4d-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ffe4d-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="ffe4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffe4d-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe4d-103">Проверка доступности данной очереди или названия темы</span><span class="sxs-lookup"><span data-stu-id="ffe4d-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="ffe4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffe4d-104">SYNTAX</span></span>

### <span data-ttu-id="ffe4d-105">QueueCheckNameAvailabilitySet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffe4d-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe4d-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ffe4d-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe4d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffe4d-107">DESCRIPTION</span></span>
<span data-ttu-id="ffe4d-108">Командлет **Test-AzServiceBusNameAvailability** проверяет доступность указанного имени очереди или темы</span><span class="sxs-lookup"><span data-stu-id="ffe4d-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="ffe4d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffe4d-109">EXAMPLES</span></span>

### <span data-ttu-id="ffe4d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ffe4d-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="ffe4d-111">Возвращает значение "истина", если указанное имя $nameQueue Availabile, или возвращает значение false, если оно указано $nameQueue недоступно.</span><span class="sxs-lookup"><span data-stu-id="ffe4d-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="ffe4d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ffe4d-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="ffe4d-113">Возвращает значение "истина", если указанное имя $nameTopic Availabile, или возвращает значение false, если оно указано $nameTopic недоступно.</span><span class="sxs-lookup"><span data-stu-id="ffe4d-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="ffe4d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffe4d-114">PARAMETERS</span></span>

### <span data-ttu-id="ffe4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe4d-115">-DefaultProfile</span></span>
<span data-ttu-id="ffe4d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffe4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe4d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffe4d-117">-Name</span></span>
<span data-ttu-id="ffe4d-118">Имя очереди для проверки доступности имени</span><span class="sxs-lookup"><span data-stu-id="ffe4d-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="ffe4d-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ffe4d-119">-Namespace</span></span>
<span data-ttu-id="ffe4d-120">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="ffe4d-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="ffe4d-121">-Очередь</span><span class="sxs-lookup"><span data-stu-id="ffe4d-121">-Queue</span></span>
<span data-ttu-id="ffe4d-122">Проверка доступности имени для имени очереди</span><span class="sxs-lookup"><span data-stu-id="ffe4d-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="ffe4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffe4d-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ffe4d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ffe4d-125">-Темы</span><span class="sxs-lookup"><span data-stu-id="ffe4d-125">-Topic</span></span>
<span data-ttu-id="ffe4d-126">Проверка доступности имени для названия темы</span><span class="sxs-lookup"><span data-stu-id="ffe4d-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="ffe4d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe4d-127">CommonParameters</span></span>
<span data-ttu-id="ffe4d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffe4d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ffe4d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe4d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe4d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffe4d-130">INPUTS</span></span>

### <span data-ttu-id="ffe4d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ffe4d-131">System.String</span></span>

## <span data-ttu-id="ffe4d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffe4d-132">OUTPUTS</span></span>

### <span data-ttu-id="ffe4d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ffe4d-133">System.Boolean</span></span>

## <span data-ttu-id="ffe4d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffe4d-134">NOTES</span></span>

## <span data-ttu-id="ffe4d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffe4d-135">RELATED LINKS</span></span>
