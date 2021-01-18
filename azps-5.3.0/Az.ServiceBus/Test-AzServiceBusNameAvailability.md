---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517321"
---
# <span data-ttu-id="d4e2f-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d4e2f-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="d4e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e2f-103">Проверка доступности заданной очереди или раздела</span><span class="sxs-lookup"><span data-stu-id="d4e2f-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="d4e2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4e2f-104">SYNTAX</span></span>

### <span data-ttu-id="d4e2f-105">QueueCheckNameAvailabilitySet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4e2f-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4e2f-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d4e2f-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4e2f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e2f-108">Проверка доступности предоставленного имени очереди или раздела с проверкой доступности для проверки доступности данной службы **AzServiceBusNameAvailability**</span><span class="sxs-lookup"><span data-stu-id="d4e2f-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="d4e2f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4e2f-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e2f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4e2f-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="d4e2f-111">Возвращает "Истина", если $nameQueue недоступна, или false, если $nameQueue недоступны.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="d4e2f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d4e2f-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="d4e2f-113">Возвращает "Истина", если $nameTopic "Предоставленный" имеет имя "Доступная", или "Ложь", $nameTopic недоступна.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="d4e2f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4e2f-114">PARAMETERS</span></span>

### <span data-ttu-id="d4e2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e2f-115">-DefaultProfile</span></span>
<span data-ttu-id="d4e2f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e2f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d4e2f-117">-Name</span></span>
<span data-ttu-id="d4e2f-118">Имя очереди для проверки доступности имени</span><span class="sxs-lookup"><span data-stu-id="d4e2f-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="d4e2f-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4e2f-119">-Namespace</span></span>
<span data-ttu-id="d4e2f-120">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="d4e2f-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="d4e2f-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="d4e2f-121">-Queue</span></span>
<span data-ttu-id="d4e2f-122">Проверка доступности имени для имени очереди</span><span class="sxs-lookup"><span data-stu-id="d4e2f-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="d4e2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4e2f-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d4e2f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d4e2f-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="d4e2f-125">-Topic</span></span>
<span data-ttu-id="d4e2f-126">Проверка доступности имени для темы</span><span class="sxs-lookup"><span data-stu-id="d4e2f-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="d4e2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e2f-127">CommonParameters</span></span>
<span data-ttu-id="d4e2f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d4e2f-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e2f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e2f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4e2f-130">INPUTS</span></span>

### <span data-ttu-id="d4e2f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d4e2f-131">System.String</span></span>

## <span data-ttu-id="d4e2f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4e2f-132">OUTPUTS</span></span>

### <span data-ttu-id="d4e2f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4e2f-133">System.Boolean</span></span>

## <span data-ttu-id="d4e2f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4e2f-134">NOTES</span></span>

## <span data-ttu-id="d4e2f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4e2f-135">RELATED LINKS</span></span>
