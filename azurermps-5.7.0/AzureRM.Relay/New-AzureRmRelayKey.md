---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567420"
---
# <span data-ttu-id="3d362-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="3d362-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="3d362-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d362-102">SYNOPSIS</span></span>
<span data-ttu-id="3d362-103">Повторно создает первичные или дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d362-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d362-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d362-104">SYNTAX</span></span>

### <span data-ttu-id="3d362-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d362-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d362-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d362-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d362-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d362-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d362-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d362-108">DESCRIPTION</span></span>
<span data-ttu-id="3d362-109">Командлет **New-AzureRmRelayKey** создает первичные и дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен и WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d362-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3d362-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d362-110">EXAMPLES</span></span>

### <span data-ttu-id="3d362-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d362-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="3d362-112">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d362-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="3d362-113">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d362-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="3d362-114">Повторно создает первичные или дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d362-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3d362-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d362-115">PARAMETERS</span></span>

### <span data-ttu-id="3d362-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d362-116">-DefaultProfile</span></span>
<span data-ttu-id="3d362-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d362-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d362-118">-HybridConnection</span></span>
<span data-ttu-id="3d362-119">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="3d362-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d362-120">-Name</span></span>
<span data-ttu-id="3d362-121">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="3d362-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3d362-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d362-122">-Namespace</span></span>
<span data-ttu-id="3d362-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3d362-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="3d362-124">-RegenerateKey</span></span>
<span data-ttu-id="3d362-125">Повторное создание ключей-"PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="3d362-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d362-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d362-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d362-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d362-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d362-128">-WcfRelay</span></span>
<span data-ttu-id="3d362-129">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="3d362-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d362-130">-Confirm</span></span>
<span data-ttu-id="3d362-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d362-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d362-132">-WhatIf</span></span>
<span data-ttu-id="3d362-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d362-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d362-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d362-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d362-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d362-135">CommonParameters</span></span>
<span data-ttu-id="3d362-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d362-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d362-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d362-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d362-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d362-138">INPUTS</span></span>

### <span data-ttu-id="3d362-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="3d362-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="3d362-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3d362-140">System.String</span></span> 

### <span data-ttu-id="3d362-141">-+ +</span><span class="sxs-lookup"><span data-stu-id="3d362-141">-NamespaceName</span></span>
 <span data-ttu-id="3d362-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3d362-142">System.String</span></span> 
 

### <span data-ttu-id="3d362-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="3d362-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="3d362-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3d362-144">System.String</span></span> 

### <span data-ttu-id="3d362-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="3d362-145">-WcfRelayName</span></span>
 <span data-ttu-id="3d362-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3d362-146">System.String</span></span> 

### <span data-ttu-id="3d362-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d362-147">-Name</span></span>
 <span data-ttu-id="3d362-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3d362-148">System.String</span></span>

### <span data-ttu-id="3d362-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="3d362-149">-RegenerateKeys</span></span>
 <span data-ttu-id="3d362-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3d362-150">System.String</span></span>

## <span data-ttu-id="3d362-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d362-151">OUTPUTS</span></span>

### <span data-ttu-id="3d362-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3d362-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="3d362-153">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d362-153">Example 1 - Namespace</span></span>
<span data-ttu-id="3d362-154">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="3d362-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="3d362-155">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d362-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="3d362-156">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="3d362-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="3d362-157">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d362-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="3d362-158">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="3d362-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="3d362-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d362-159">NOTES</span></span>

## <span data-ttu-id="3d362-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d362-160">RELATED LINKS</span></span>

