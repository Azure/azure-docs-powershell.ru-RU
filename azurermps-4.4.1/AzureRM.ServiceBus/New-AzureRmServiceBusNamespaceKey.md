---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567052"
---
# <span data-ttu-id="42bad-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="42bad-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="42bad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42bad-102">SYNOPSIS</span></span>
<span data-ttu-id="42bad-103">Повторно создает первичные или дополнительные строки подключения для пространства имен Service Bus.</span><span class="sxs-lookup"><span data-stu-id="42bad-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42bad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42bad-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42bad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42bad-105">DESCRIPTION</span></span>
<span data-ttu-id="42bad-106">Командлет **New-AzureRmServiceBusNamespace** создает новые первичные или дополнительные строки подключения для указанного пространства имен и правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="42bad-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="42bad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42bad-107">EXAMPLES</span></span>

### <span data-ttu-id="42bad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42bad-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="42bad-109">Повторно создает первичные или дополнительные строки подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="42bad-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="42bad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42bad-110">PARAMETERS</span></span>

### <span data-ttu-id="42bad-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="42bad-111">-RegenerateKeys</span></span>
<span data-ttu-id="42bad-112">Повторное создание ключей: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="42bad-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="42bad-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42bad-113">-ResourceGroup</span></span>
<span data-ttu-id="42bad-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42bad-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42bad-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42bad-115">-Confirm</span></span>
<span data-ttu-id="42bad-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42bad-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bad-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42bad-117">-WhatIf</span></span>
<span data-ttu-id="42bad-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42bad-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42bad-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42bad-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bad-120">-DefaultProfile</span></span>
<span data-ttu-id="42bad-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42bad-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42bad-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42bad-122">-Name</span></span>
<span data-ttu-id="42bad-123">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="42bad-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="42bad-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="42bad-124">-Namespace</span></span>
<span data-ttu-id="42bad-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="42bad-125">Namespace Name.</span></span>

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

### <span data-ttu-id="42bad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bad-126">CommonParameters</span></span>
<span data-ttu-id="42bad-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42bad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bad-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42bad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bad-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42bad-129">INPUTS</span></span>

### <span data-ttu-id="42bad-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42bad-130">-ResourceGroup</span></span>
 <span data-ttu-id="42bad-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42bad-131">System.String</span></span>
 

### <span data-ttu-id="42bad-132">-+ +</span><span class="sxs-lookup"><span data-stu-id="42bad-132">-NamespaceName</span></span>
 <span data-ttu-id="42bad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="42bad-133">System.String</span></span>
 

### <span data-ttu-id="42bad-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="42bad-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="42bad-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42bad-135">System.String</span></span>
 

### <span data-ttu-id="42bad-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="42bad-136">-RegenerateKeys</span></span>
 <span data-ttu-id="42bad-137">System. String</span><span class="sxs-lookup"><span data-stu-id="42bad-137">System.String</span></span>

## <span data-ttu-id="42bad-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42bad-138">OUTPUTS</span></span>

### <span data-ttu-id="42bad-139">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="42bad-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="42bad-140">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-value} SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-value} PrimaryKey: {значение PrimaryKey value} SecondaryKey: {SecondaryKey value} KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="42bad-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="42bad-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="42bad-141">NOTES</span></span>

## <span data-ttu-id="42bad-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42bad-142">RELATED LINKS</span></span>

