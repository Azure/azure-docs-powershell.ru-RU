---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410511"
---
# <span data-ttu-id="95eea-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="95eea-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="95eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95eea-102">SYNOPSIS</span></span>
<span data-ttu-id="95eea-103">Возвращает строки основного и дополнительного подключения для заданной сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="95eea-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="95eea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95eea-104">SYNTAX</span></span>

### <span data-ttu-id="95eea-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95eea-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95eea-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="95eea-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95eea-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="95eea-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95eea-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95eea-108">DESCRIPTION</span></span>
<span data-ttu-id="95eea-109">Командлет **Get-AzRelayKey** возвращает строки основного и дополнительного подключения для заданной сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="95eea-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="95eea-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95eea-110">EXAMPLES</span></span>

### <span data-ttu-id="95eea-111">Пример 1. Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95eea-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="95eea-112">Пример 2. WcfRelay</span><span class="sxs-lookup"><span data-stu-id="95eea-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="95eea-113">Пример 3. Гибриднаясоединение</span><span class="sxs-lookup"><span data-stu-id="95eea-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="95eea-114">Строка основного и дополнительного подключения к указанным объектам relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="95eea-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="95eea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95eea-115">PARAMETERS</span></span>

### <span data-ttu-id="95eea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95eea-116">-DefaultProfile</span></span>
<span data-ttu-id="95eea-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95eea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95eea-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="95eea-118">-HybridConnection</span></span>
<span data-ttu-id="95eea-119">Имя HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="95eea-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="95eea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="95eea-120">-Name</span></span>
<span data-ttu-id="95eea-121">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="95eea-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="95eea-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="95eea-122">-Namespace</span></span>
<span data-ttu-id="95eea-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="95eea-123">Namespace Name.</span></span>

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

### <span data-ttu-id="95eea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95eea-124">-ResourceGroupName</span></span>
<span data-ttu-id="95eea-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95eea-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="95eea-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="95eea-126">-WcfRelay</span></span>
<span data-ttu-id="95eea-127">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="95eea-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="95eea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95eea-128">CommonParameters</span></span>
<span data-ttu-id="95eea-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95eea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95eea-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95eea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95eea-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95eea-131">INPUTS</span></span>

### <span data-ttu-id="95eea-132">System.String</span><span class="sxs-lookup"><span data-stu-id="95eea-132">System.String</span></span>

## <span data-ttu-id="95eea-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95eea-133">OUTPUTS</span></span>

### <span data-ttu-id="95eea-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="95eea-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="95eea-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95eea-135">NOTES</span></span>

## <span data-ttu-id="95eea-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95eea-136">RELATED LINKS</span></span>