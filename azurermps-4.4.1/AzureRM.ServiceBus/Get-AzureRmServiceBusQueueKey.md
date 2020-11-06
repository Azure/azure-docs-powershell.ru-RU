---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567507"
---
# <span data-ttu-id="23361-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="23361-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="23361-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23361-102">SYNOPSIS</span></span>
<span data-ttu-id="23361-103">Получает первичные и дополнительные строки подключения для заданной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="23361-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23361-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23361-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23361-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23361-105">DESCRIPTION</span></span>
<span data-ttu-id="23361-106">Командлет **Get-AzureRmServiceBusQueueKey** Возвращает основную и вспомогательную строки подключения для заданной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="23361-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="23361-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23361-107">EXAMPLES</span></span>

### <span data-ttu-id="23361-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23361-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="23361-109">Возвращает основную и вспомогательную строки подключения для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="23361-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="23361-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23361-110">PARAMETERS</span></span>

### <span data-ttu-id="23361-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23361-111">-ResourceGroup</span></span>
<span data-ttu-id="23361-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23361-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23361-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23361-113">-DefaultProfile</span></span>
<span data-ttu-id="23361-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23361-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23361-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23361-115">-Name</span></span>
<span data-ttu-id="23361-116">ServiceBus AuthorizationRule имя очереди.</span><span class="sxs-lookup"><span data-stu-id="23361-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23361-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23361-117">-Namespace</span></span>
<span data-ttu-id="23361-118">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="23361-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23361-119">-Очередь</span><span class="sxs-lookup"><span data-stu-id="23361-119">-Queue</span></span>
<span data-ttu-id="23361-120">Имя очереди ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="23361-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23361-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23361-121">CommonParameters</span></span>
<span data-ttu-id="23361-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23361-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23361-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23361-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23361-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23361-124">INPUTS</span></span>

### <span data-ttu-id="23361-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23361-125">-ResourceGroup</span></span>
 <span data-ttu-id="23361-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23361-126">System.String</span></span>
 

### <span data-ttu-id="23361-127">-+ +</span><span class="sxs-lookup"><span data-stu-id="23361-127">-NamespaceName</span></span>
 <span data-ttu-id="23361-128">System. String</span><span class="sxs-lookup"><span data-stu-id="23361-128">System.String</span></span>
 

### <span data-ttu-id="23361-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="23361-129">-QueueName</span></span>
 <span data-ttu-id="23361-130">System. String</span><span class="sxs-lookup"><span data-stu-id="23361-130">System.String</span></span>
 

### <span data-ttu-id="23361-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="23361-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="23361-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23361-132">System.String</span></span>

## <span data-ttu-id="23361-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23361-133">OUTPUTS</span></span>

### <span data-ttu-id="23361-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="23361-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="23361-135">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {value PrimaryKey} SecondaryKey: {SecondaryKey значение} KeyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="23361-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="23361-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="23361-136">NOTES</span></span>

## <span data-ttu-id="23361-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23361-137">RELATED LINKS</span></span>

