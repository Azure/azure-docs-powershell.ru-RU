---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 7394ec382105b1d05bed589be95630f68ab79ae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567528"
---
# <span data-ttu-id="bfbfd-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="bfbfd-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="bfbfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbfd-103">Повторно создает первичные или дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="bfbfd-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfbfd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfbfd-104">SYNTAX</span></span>

### <span data-ttu-id="bfbfd-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfbfd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbfd-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfbfd-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbfd-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfbfd-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfbfd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfbfd-108">DESCRIPTION</span></span>
<span data-ttu-id="bfbfd-109">Командлет **New-AzureRmRelayKey** создает первичные и дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен и WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="bfbfd-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="bfbfd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfbfd-110">EXAMPLES</span></span>

### <span data-ttu-id="bfbfd-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="bfbfd-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="bfbfd-112">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="bfbfd-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="bfbfd-113">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="bfbfd-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="bfbfd-114">Повторно создает первичные или дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="bfbfd-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="bfbfd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfbfd-115">PARAMETERS</span></span>

### <span data-ttu-id="bfbfd-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfbfd-116">-Confirm</span></span>
<span data-ttu-id="bfbfd-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbfd-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="bfbfd-118">-HybridConnection</span></span>
<span data-ttu-id="bfbfd-119">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-119">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbfd-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfbfd-120">-Name</span></span>
<span data-ttu-id="bfbfd-121">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-121">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbfd-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bfbfd-122">-Namespace</span></span>
<span data-ttu-id="bfbfd-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-123">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbfd-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="bfbfd-124">-RegenerateKey</span></span>
<span data-ttu-id="bfbfd-125">Повторное создание ключей-"PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="bfbfd-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfbfd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfbfd-126">-ResourceGroupName</span></span>
<span data-ttu-id="bfbfd-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="bfbfd-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="bfbfd-128">-WcfRelay</span></span>
<span data-ttu-id="bfbfd-129">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbfd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbfd-130">-WhatIf</span></span>
<span data-ttu-id="bfbfd-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfbfd-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbfd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbfd-133">-DefaultProfile</span></span>
<span data-ttu-id="bfbfd-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfbfd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbfd-135">CommonParameters</span></span>
<span data-ttu-id="bfbfd-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfbfd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbfd-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfbfd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbfd-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfbfd-138">INPUTS</span></span>

### <span data-ttu-id="bfbfd-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="bfbfd-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="bfbfd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbfd-140">System.String</span></span> 

### <span data-ttu-id="bfbfd-141">-+ +</span><span class="sxs-lookup"><span data-stu-id="bfbfd-141">-NamespaceName</span></span>
 <span data-ttu-id="bfbfd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbfd-142">System.String</span></span> 
 

### <span data-ttu-id="bfbfd-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="bfbfd-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="bfbfd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbfd-144">System.String</span></span> 

### <span data-ttu-id="bfbfd-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="bfbfd-145">-WcfRelayName</span></span>
 <span data-ttu-id="bfbfd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbfd-146">System.String</span></span> 

### <span data-ttu-id="bfbfd-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfbfd-147">-Name</span></span>
 <span data-ttu-id="bfbfd-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbfd-148">System.String</span></span>

### <span data-ttu-id="bfbfd-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="bfbfd-149">-RegenerateKeys</span></span>
 <span data-ttu-id="bfbfd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbfd-150">System.String</span></span>

## <span data-ttu-id="bfbfd-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfbfd-151">OUTPUTS</span></span>

### <span data-ttu-id="bfbfd-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="bfbfd-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="bfbfd-153">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="bfbfd-153">Example 1 - Namespace</span></span>
<span data-ttu-id="bfbfd-154">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="bfbfd-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="bfbfd-155">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="bfbfd-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="bfbfd-156">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="bfbfd-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="bfbfd-157">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="bfbfd-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="bfbfd-158">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="bfbfd-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="bfbfd-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfbfd-159">NOTES</span></span>

## <span data-ttu-id="bfbfd-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfbfd-160">RELATED LINKS</span></span>

