---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562167"
---
# <span data-ttu-id="4bd7c-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="4bd7c-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="4bd7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd7c-103">Повторно создает первичные или дополнительные строки подключения для раздела служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bd7c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bd7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd7c-106">Командлет **New-AzureRmServiceBusTopicKey** создает новую первичную или вспомогательную строку подключения для указанной темы служебной шины и правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="4bd7c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bd7c-107">EXAMPLES</span></span>

### <span data-ttu-id="4bd7c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4bd7c-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="4bd7c-109">Повторно создает основную строку подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="4bd7c-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4bd7c-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="4bd7c-111">Повторно создает вспомогательную строку подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="4bd7c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bd7c-112">PARAMETERS</span></span>

### <span data-ttu-id="4bd7c-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="4bd7c-113">-RegenerateKeys</span></span>
<span data-ttu-id="4bd7c-114">Указывает, следует ли повторно создавать первичные или вторичные ключи.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4bd7c-115">-ResourceGroup</span></span>
<span data-ttu-id="4bd7c-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bd7c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bd7c-117">-Confirm</span></span>
<span data-ttu-id="4bd7c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd7c-119">-WhatIf</span></span>
<span data-ttu-id="4bd7c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd7c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd7c-122">-DefaultProfile</span></span>
<span data-ttu-id="4bd7c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd7c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4bd7c-124">-Name</span></span>
<span data-ttu-id="4bd7c-125">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-125">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="4bd7c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4bd7c-126">-Namespace</span></span>
<span data-ttu-id="4bd7c-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-127">Namespace Name.</span></span>

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

### <span data-ttu-id="4bd7c-128">-Темы</span><span class="sxs-lookup"><span data-stu-id="4bd7c-128">-Topic</span></span>
<span data-ttu-id="4bd7c-129">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd7c-130">CommonParameters</span></span>
<span data-ttu-id="4bd7c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd7c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd7c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd7c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bd7c-133">INPUTS</span></span>

### <span data-ttu-id="4bd7c-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4bd7c-134">-ResourceGroup</span></span>
 <span data-ttu-id="4bd7c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd7c-135">System.String</span></span>
 

### <span data-ttu-id="4bd7c-136">-+ +</span><span class="sxs-lookup"><span data-stu-id="4bd7c-136">-NamespaceName</span></span>
 <span data-ttu-id="4bd7c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd7c-137">System.String</span></span>
 

### <span data-ttu-id="4bd7c-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4bd7c-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="4bd7c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd7c-139">System.String</span></span>
 

### <span data-ttu-id="4bd7c-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4bd7c-140">-TopicName</span></span>
 <span data-ttu-id="4bd7c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd7c-141">System.String</span></span>
 

### <span data-ttu-id="4bd7c-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="4bd7c-142">-RegenerateKeys</span></span>
 <span data-ttu-id="4bd7c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd7c-143">System.String</span></span>

## <span data-ttu-id="4bd7c-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bd7c-144">OUTPUTS</span></span>

### <span data-ttu-id="4bd7c-145">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4bd7c-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="4bd7c-146">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Topi c_exampl1 PrimaryKey: {value PrimaryKey} SecondaryKey: {SecondaryKey значение} KeyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="4bd7c-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="4bd7c-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bd7c-147">NOTES</span></span>

## <span data-ttu-id="4bd7c-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bd7c-148">RELATED LINKS</span></span>

