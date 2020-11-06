---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 897ecd66665091fd3be1f14b31c00549912a0af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558852"
---
# <span data-ttu-id="fb542-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="fb542-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="fb542-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb542-102">SYNOPSIS</span></span>
<span data-ttu-id="fb542-103">Получает первичные и дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fb542-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb542-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb542-104">SYNTAX</span></span>

### <span data-ttu-id="fb542-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb542-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb542-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb542-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb542-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb542-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb542-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb542-108">DESCRIPTION</span></span>
<span data-ttu-id="fb542-109">Командлет **Get-AzureRmRelayKey** возвращает первичные и дополнительные строки подключения для указанных ретранслируемых сущностей (пространство имен и WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fb542-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fb542-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb542-110">EXAMPLES</span></span>

### <span data-ttu-id="fb542-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="fb542-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="fb542-112">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fb542-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="fb542-113">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fb542-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="fb542-114">Основной и дополнительный строки соединения с указанными ретранслируемыми сущностями (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fb542-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fb542-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb542-115">PARAMETERS</span></span>

### <span data-ttu-id="fb542-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb542-116">-DefaultProfile</span></span>
<span data-ttu-id="fb542-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb542-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb542-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fb542-118">-HybridConnection</span></span>
<span data-ttu-id="fb542-119">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="fb542-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="fb542-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb542-120">-Name</span></span>
<span data-ttu-id="fb542-121">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="fb542-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="fb542-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb542-122">-Namespace</span></span>
<span data-ttu-id="fb542-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fb542-123">Namespace Name.</span></span>

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

### <span data-ttu-id="fb542-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb542-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb542-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb542-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb542-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fb542-126">-WcfRelay</span></span>
<span data-ttu-id="fb542-127">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="fb542-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="fb542-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb542-128">CommonParameters</span></span>
<span data-ttu-id="fb542-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb542-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb542-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb542-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb542-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb542-131">INPUTS</span></span>

### <span data-ttu-id="fb542-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb542-132">-ResourceGroupName</span></span>
 <span data-ttu-id="fb542-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fb542-133">System.String</span></span> 

### <span data-ttu-id="fb542-134">-+ +</span><span class="sxs-lookup"><span data-stu-id="fb542-134">-NamespaceName</span></span>
 <span data-ttu-id="fb542-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fb542-135">System.String</span></span> 
 

### <span data-ttu-id="fb542-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="fb542-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="fb542-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fb542-137">System.String</span></span> 

### <span data-ttu-id="fb542-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="fb542-138">-WcfRelayName</span></span>
 <span data-ttu-id="fb542-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fb542-139">System.String</span></span> 

### <span data-ttu-id="fb542-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb542-140">-Name</span></span>
 <span data-ttu-id="fb542-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fb542-141">System.String</span></span>

## <span data-ttu-id="fb542-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb542-142">OUTPUTS</span></span>

### <span data-ttu-id="fb542-143">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="fb542-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="fb542-144">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="fb542-144">Example 1 - Namespace</span></span>
<span data-ttu-id="fb542-145">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="fb542-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="fb542-146">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fb542-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="fb542-147">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="fb542-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="fb542-148">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fb542-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="fb542-149">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # выAuthoRule1:</span><span class="sxs-lookup"><span data-stu-id="fb542-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="fb542-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb542-150">NOTES</span></span>

## <span data-ttu-id="fb542-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb542-151">RELATED LINKS</span></span>

