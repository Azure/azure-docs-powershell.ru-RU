---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505989"
---
# <span data-ttu-id="dc8fc-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc8fc-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="dc8fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8fc-103">Создает гибриднуюсоединение в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="dc8fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc8fc-104">SYNTAX</span></span>

### <span data-ttu-id="dc8fc-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc8fc-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc8fc-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dc8fc-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc8fc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc8fc-107">DESCRIPTION</span></span>
<span data-ttu-id="dc8fc-108">Командлет New-AzRelayHybridConnection создает гибридное подключение в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="dc8fc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc8fc-109">EXAMPLES</span></span>

### <span data-ttu-id="dc8fc-110">Пример 1. InputObject</span><span class="sxs-lookup"><span data-stu-id="dc8fc-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="dc8fc-111">Создает новое решение HybirdConnection TestHybirdConnection2 в указанной области имен ретрансляции \` \` \` TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="dc8fc-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="dc8fc-112">Пример 2. Свойства</span><span class="sxs-lookup"><span data-stu-id="dc8fc-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="dc8fc-113">Создает новое решение HybirdConnection TestHybirdConnection1 в указанной области имен ретрансляции \` \` \` TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="dc8fc-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="dc8fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc8fc-114">PARAMETERS</span></span>

### <span data-ttu-id="dc8fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8fc-115">-DefaultProfile</span></span>
<span data-ttu-id="dc8fc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8fc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc8fc-117">-InputObject</span></span>
<span data-ttu-id="dc8fc-118">Объект HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8fc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dc8fc-119">-Name</span></span>
<span data-ttu-id="dc8fc-120">Имя HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="dc8fc-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc8fc-121">-Namespace</span></span>
<span data-ttu-id="dc8fc-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-122">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8fc-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="dc8fc-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="dc8fc-124">true, если для этого подключения HybridConnections требуется авторизация клиента; в противном случае ложь</span><span class="sxs-lookup"><span data-stu-id="dc8fc-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc8fc-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc8fc-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="dc8fc-127">-UserMetadata</span></span>
<span data-ttu-id="dc8fc-128">Gets or sets usermetadata — это место для хранения пользовательских строковые данных для конечной точки HybridConnection. его можно использовать для хранения описательных данных, таких как список групп и их контактные данные, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8fc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc8fc-129">-Confirm</span></span>
<span data-ttu-id="dc8fc-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc8fc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc8fc-131">-WhatIf</span></span>
<span data-ttu-id="dc8fc-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc8fc-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc8fc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8fc-134">CommonParameters</span></span>
<span data-ttu-id="dc8fc-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8fc-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc8fc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8fc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc8fc-137">INPUTS</span></span>

### <span data-ttu-id="dc8fc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dc8fc-138">System.String</span></span>

### <span data-ttu-id="dc8fc-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="dc8fc-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="dc8fc-140">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dc8fc-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dc8fc-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc8fc-141">OUTPUTS</span></span>

### <span data-ttu-id="dc8fc-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="dc8fc-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="dc8fc-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc8fc-143">NOTES</span></span>

## <span data-ttu-id="dc8fc-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc8fc-144">RELATED LINKS</span></span>
