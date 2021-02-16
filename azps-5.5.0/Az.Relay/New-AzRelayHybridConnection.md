---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240117"
---
# <span data-ttu-id="d160d-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="d160d-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="d160d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d160d-102">SYNOPSIS</span></span>
<span data-ttu-id="d160d-103">Создает гибриднуюсоединение в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="d160d-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d160d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d160d-104">SYNTAX</span></span>

### <span data-ttu-id="d160d-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d160d-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d160d-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d160d-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d160d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d160d-107">DESCRIPTION</span></span>
<span data-ttu-id="d160d-108">Командлет New-AzRelayHybridConnection создает гибридное подключение в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="d160d-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d160d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d160d-109">EXAMPLES</span></span>

### <span data-ttu-id="d160d-110">Пример 1. InputObject</span><span class="sxs-lookup"><span data-stu-id="d160d-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="d160d-111">Создает новое решение HybirdConnection TestHybirdConnection2 в указанной области имен ретрансляции \` \` \` TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="d160d-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="d160d-112">Пример 2. Свойства</span><span class="sxs-lookup"><span data-stu-id="d160d-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="d160d-113">Создает новое решение HybirdConnection TestHybirdConnection1 в указанной области имен ретрансляции \` \` \` TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="d160d-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="d160d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d160d-114">PARAMETERS</span></span>

### <span data-ttu-id="d160d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d160d-115">-DefaultProfile</span></span>
<span data-ttu-id="d160d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d160d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d160d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d160d-117">-InputObject</span></span>
<span data-ttu-id="d160d-118">Объект HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="d160d-118">HybridConnections object.</span></span>

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

### <span data-ttu-id="d160d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d160d-119">-Name</span></span>
<span data-ttu-id="d160d-120">Имя HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="d160d-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="d160d-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d160d-121">-Namespace</span></span>
<span data-ttu-id="d160d-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d160d-122">Namespace Name.</span></span>

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

### <span data-ttu-id="d160d-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="d160d-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="d160d-124">true, если для этого подключения HybridConnections требуется авторизация клиента; в противном случае ложь</span><span class="sxs-lookup"><span data-stu-id="d160d-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="d160d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d160d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d160d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d160d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="d160d-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d160d-127">-UserMetadata</span></span>
<span data-ttu-id="d160d-128">Gets or sets usermetadata — это место для хранения пользовательских строковые данных для конечной точки HybridConnection. его можно использовать для хранения описательных данных, таких как список групп и их контактные данные, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d160d-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="d160d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d160d-129">-Confirm</span></span>
<span data-ttu-id="d160d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d160d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d160d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d160d-131">-WhatIf</span></span>
<span data-ttu-id="d160d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d160d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d160d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d160d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d160d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d160d-134">CommonParameters</span></span>
<span data-ttu-id="d160d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d160d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d160d-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d160d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d160d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d160d-137">INPUTS</span></span>

### <span data-ttu-id="d160d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d160d-138">System.String</span></span>

### <span data-ttu-id="d160d-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="d160d-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="d160d-140">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d160d-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d160d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d160d-141">OUTPUTS</span></span>

### <span data-ttu-id="d160d-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="d160d-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="d160d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d160d-143">NOTES</span></span>

## <span data-ttu-id="d160d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d160d-144">RELATED LINKS</span></span>
