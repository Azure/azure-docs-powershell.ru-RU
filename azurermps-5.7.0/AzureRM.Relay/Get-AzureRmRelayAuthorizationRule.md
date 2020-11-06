---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 333e3eeaaf7655c78d557eb104fa4a349a0c05e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558855"
---
# <span data-ttu-id="1d82b-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d82b-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="1d82b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d82b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d82b-103">Возвращает описание указанного правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1d82b-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d82b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d82b-104">SYNTAX</span></span>

### <span data-ttu-id="1d82b-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d82b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d82b-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d82b-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d82b-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d82b-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d82b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d82b-108">DESCRIPTION</span></span>
<span data-ttu-id="1d82b-109">Командлет **Get-AzureRmRelayAuthorizationRule** получает описание указанного правила авторизации в заданных сущностях ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1d82b-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1d82b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d82b-110">EXAMPLES</span></span>

### <span data-ttu-id="1d82b-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d82b-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="1d82b-112">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1d82b-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="1d82b-113">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1d82b-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="1d82b-114">Возвращает указанное описание правила авторизации для данного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="1d82b-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="1d82b-115">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1d82b-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="1d82b-116">Возвращает указанное описание правила авторизации для данного HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1d82b-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="1d82b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d82b-117">PARAMETERS</span></span>

### <span data-ttu-id="1d82b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d82b-118">-DefaultProfile</span></span>
<span data-ttu-id="1d82b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d82b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d82b-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1d82b-120">-HybridConnection</span></span>
<span data-ttu-id="1d82b-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="1d82b-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="1d82b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d82b-122">-Name</span></span>
<span data-ttu-id="1d82b-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="1d82b-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d82b-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d82b-124">-Namespace</span></span>
<span data-ttu-id="1d82b-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1d82b-125">Namespace Name.</span></span>

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

### <span data-ttu-id="1d82b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d82b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1d82b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d82b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="1d82b-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1d82b-128">-WcfRelay</span></span>
<span data-ttu-id="1d82b-129">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="1d82b-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="1d82b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d82b-130">CommonParameters</span></span>
<span data-ttu-id="1d82b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d82b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d82b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d82b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d82b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d82b-133">INPUTS</span></span>

### <span data-ttu-id="1d82b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d82b-134">-ResourceGroupName</span></span>
 <span data-ttu-id="1d82b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1d82b-135">System.String</span></span> 

### <span data-ttu-id="1d82b-136">-+ +</span><span class="sxs-lookup"><span data-stu-id="1d82b-136">-NamespaceName</span></span>
 <span data-ttu-id="1d82b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1d82b-137">System.String</span></span> 
 

### <span data-ttu-id="1d82b-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="1d82b-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="1d82b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1d82b-139">System.String</span></span> 

### <span data-ttu-id="1d82b-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="1d82b-140">-WcfRelayName</span></span>
 <span data-ttu-id="1d82b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1d82b-141">System.String</span></span> 

### <span data-ttu-id="1d82b-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d82b-142">-Name</span></span>
 <span data-ttu-id="1d82b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1d82b-143">System.String</span></span>

## <span data-ttu-id="1d82b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d82b-144">OUTPUTS</span></span>

### <span data-ttu-id="1d82b-145">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Model. AuthorizationRuleAttributes, Microsoft. Azure. Commands. ретрансляцией, Version = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1d82b-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1d82b-146">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d82b-146">Example 1 - Namespace</span></span>
<span data-ttu-id="1d82b-147">Права: {Listen, Send} Name: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="1d82b-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="1d82b-148">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1d82b-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="1d82b-149">Права: {Listen, Send} Name: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1d82b-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="1d82b-150">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1d82b-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="1d82b-151">Права: {Listen, Send} Name: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1d82b-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="1d82b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d82b-152">NOTES</span></span>

## <span data-ttu-id="1d82b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d82b-153">RELATED LINKS</span></span>

