---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242648"
---
# <span data-ttu-id="38f53-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="38f53-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="38f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f53-102">SYNOPSIS</span></span>
<span data-ttu-id="38f53-103">Создает WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="38f53-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="38f53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38f53-104">SYNTAX</span></span>

### <span data-ttu-id="38f53-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38f53-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38f53-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="38f53-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f53-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38f53-107">DESCRIPTION</span></span>
<span data-ttu-id="38f53-108">Командлет New-AzWcfRelay создает WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="38f53-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="38f53-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38f53-109">EXAMPLES</span></span>

### <span data-ttu-id="38f53-110">Пример 1. InputObject</span><span class="sxs-lookup"><span data-stu-id="38f53-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="38f53-111">Создает новую WcfRelay TestWCFRelay2 в указанной области имен \` \` ретрансляции \` TestNameSpace-Relay. \`</span><span class="sxs-lookup"><span data-stu-id="38f53-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="38f53-112">Пример 2. Свойства</span><span class="sxs-lookup"><span data-stu-id="38f53-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="38f53-113">Создает новую WcfRelay TestWCFRelay в указанной области имен ретрансляции \` \` \` TestNameSpace-Relay1. \`</span><span class="sxs-lookup"><span data-stu-id="38f53-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="38f53-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38f53-114">PARAMETERS</span></span>

### <span data-ttu-id="38f53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f53-115">-DefaultProfile</span></span>
<span data-ttu-id="38f53-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38f53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38f53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38f53-117">-InputObject</span></span>
<span data-ttu-id="38f53-118">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="38f53-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f53-119">-Name</span><span class="sxs-lookup"><span data-stu-id="38f53-119">-Name</span></span>
<span data-ttu-id="38f53-120">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="38f53-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f53-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="38f53-121">-Namespace</span></span>
<span data-ttu-id="38f53-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="38f53-122">Namespace Name.</span></span>

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

### <span data-ttu-id="38f53-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="38f53-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="38f53-124">true, если для этой ретрансляции требуется авторизация клиента; в противном случае ложь</span><span class="sxs-lookup"><span data-stu-id="38f53-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f53-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="38f53-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="38f53-126">имеет true, если для этой ретрансляции требуется безопасность транспорта; в противном случае ложь</span><span class="sxs-lookup"><span data-stu-id="38f53-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f53-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f53-127">-ResourceGroupName</span></span>
<span data-ttu-id="38f53-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38f53-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="38f53-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="38f53-129">-UserMetadata</span></span>
<span data-ttu-id="38f53-130">Gets or sets usermetadata — это место для хранения пользовательских строковые данных для конечной точки HybridConnection. его можно использовать для хранения описательных данных, таких как список групп и их контактные данные, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="38f53-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f53-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="38f53-131">-WcfRelayType</span></span>
<span data-ttu-id="38f53-132">WcfRelay Type.</span><span class="sxs-lookup"><span data-stu-id="38f53-132">WcfRelay Type.</span></span>
<span data-ttu-id="38f53-133">Возможные значения: NetTcp или http</span><span class="sxs-lookup"><span data-stu-id="38f53-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f53-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38f53-134">-Confirm</span></span>
<span data-ttu-id="38f53-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="38f53-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f53-136">-WhatIf</span></span>
<span data-ttu-id="38f53-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f53-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f53-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38f53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f53-139">CommonParameters</span></span>
<span data-ttu-id="38f53-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f53-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f53-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f53-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38f53-142">INPUTS</span></span>

### <span data-ttu-id="38f53-143">System.String</span><span class="sxs-lookup"><span data-stu-id="38f53-143">System.String</span></span>

### <span data-ttu-id="38f53-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="38f53-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="38f53-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38f53-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="38f53-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38f53-146">OUTPUTS</span></span>

### <span data-ttu-id="38f53-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="38f53-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="38f53-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38f53-148">NOTES</span></span>

## <span data-ttu-id="38f53-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38f53-149">RELATED LINKS</span></span>
