---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734772"
---
# <span data-ttu-id="a4dd7-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="a4dd7-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="a4dd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dd7-103">Повторно создает первичные или дополнительные строки подключения для очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4dd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4dd7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4dd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="a4dd7-106">Командлет **New-AzureRmServiceBusQueueKey** заново создает первичные или дополнительные строки подключения для указанной очереди обслуживания служебной шины и правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="a4dd7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-107">EXAMPLES</span></span>

### <span data-ttu-id="a4dd7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4dd7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="a4dd7-109">Повторно создает основную строку подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="a4dd7-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a4dd7-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="a4dd7-111">Повторно создает вспомогательную строку подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="a4dd7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-112">PARAMETERS</span></span>

### <span data-ttu-id="a4dd7-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a4dd7-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="a4dd7-114">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4dd7-115">-+ +</span><span class="sxs-lookup"><span data-stu-id="a4dd7-115">-NamespaceName</span></span>
<span data-ttu-id="a4dd7-116">Имя пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="a4dd7-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="a4dd7-117">-QueueName</span></span>
<span data-ttu-id="a4dd7-118">Имя очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-118">The Service Bus queue name.</span></span>

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

### <span data-ttu-id="a4dd7-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="a4dd7-119">-RegenerateKeys</span></span>
<span data-ttu-id="a4dd7-120">Указывает, следует ли повторно создавать первичные или вторичные ключи.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dd7-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4dd7-121">-ResourceGroup</span></span>
<span data-ttu-id="a4dd7-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4dd7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4dd7-123">-Confirm</span></span>
<span data-ttu-id="a4dd7-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dd7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dd7-125">-WhatIf</span></span>
<span data-ttu-id="a4dd7-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dd7-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dd7-128">CommonParameters</span></span>
<span data-ttu-id="a4dd7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dd7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dd7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4dd7-131">INPUTS</span></span>

### <span data-ttu-id="a4dd7-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4dd7-132">-ResourceGroup</span></span>
 <span data-ttu-id="a4dd7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dd7-133">System.String</span></span>
 

### <span data-ttu-id="a4dd7-134">-+ +</span><span class="sxs-lookup"><span data-stu-id="a4dd7-134">-NamespaceName</span></span>
 <span data-ttu-id="a4dd7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dd7-135">System.String</span></span>
 

### <span data-ttu-id="a4dd7-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a4dd7-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="a4dd7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dd7-137">System.String</span></span>
 

### <span data-ttu-id="a4dd7-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="a4dd7-138">-QueueName</span></span>
 <span data-ttu-id="a4dd7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dd7-139">System.String</span></span>
 

### <span data-ttu-id="a4dd7-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="a4dd7-140">-RegenerateKeys</span></span>
 <span data-ttu-id="a4dd7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dd7-141">System.String</span></span>

## <span data-ttu-id="a4dd7-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-142">OUTPUTS</span></span>

### <span data-ttu-id="a4dd7-143">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="a4dd7-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="a4dd7-144">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {value PrimaryKey} SecondaryKey: {SecondaryKey значение} KeyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="a4dd7-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="a4dd7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4dd7-145">NOTES</span></span>

## <span data-ttu-id="a4dd7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-146">RELATED LINKS</span></span>

