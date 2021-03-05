---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 85c8d65f8a690f9cc977ff069fe6972f5537a114
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000360"
---
# <span data-ttu-id="a1fb2-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="a1fb2-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="a1fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fb2-103">Обновляет описание WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="a1fb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1fb2-104">SYNTAX</span></span>

### <span data-ttu-id="a1fb2-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1fb2-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1fb2-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a1fb2-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1fb2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1fb2-107">DESCRIPTION</span></span>
<span data-ttu-id="a1fb2-108">Командлет Set-AzWcfRelay обновляет описание WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="a1fb2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1fb2-109">EXAMPLES</span></span>

### <span data-ttu-id="a1fb2-110">Пример 1. InputObject</span><span class="sxs-lookup"><span data-stu-id="a1fb2-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="a1fb2-111">Пример 2. Свойства</span><span class="sxs-lookup"><span data-stu-id="a1fb2-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
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

<span data-ttu-id="a1fb2-112">Обновление указанного WcfRelay с новым описанием в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="a1fb2-113">В этом примере свойство UserMetadata обновляется на новое значение.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="a1fb2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1fb2-114">PARAMETERS</span></span>

### <span data-ttu-id="a1fb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fb2-115">-DefaultProfile</span></span>
<span data-ttu-id="a1fb2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1fb2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1fb2-117">-InputObject</span></span>
<span data-ttu-id="a1fb2-118">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="a1fb2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a1fb2-119">-Name</span></span>
<span data-ttu-id="a1fb2-120">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a1fb2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a1fb2-121">-Namespace</span></span>
<span data-ttu-id="a1fb2-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-122">Namespace Name.</span></span>

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

### <span data-ttu-id="a1fb2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1fb2-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1fb2-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1fb2-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a1fb2-125">-UserMetadata</span></span>
<span data-ttu-id="a1fb2-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.g. его можно использовать для хранения описательных данных, таких как список групп и их контактные данные, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="a1fb2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1fb2-127">-Confirm</span></span>
<span data-ttu-id="a1fb2-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1fb2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1fb2-129">-WhatIf</span></span>
<span data-ttu-id="a1fb2-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1fb2-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1fb2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fb2-132">CommonParameters</span></span>
<span data-ttu-id="a1fb2-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fb2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fb2-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1fb2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fb2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1fb2-135">INPUTS</span></span>

### <span data-ttu-id="a1fb2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a1fb2-136">System.String</span></span>

### <span data-ttu-id="a1fb2-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="a1fb2-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="a1fb2-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1fb2-138">OUTPUTS</span></span>

### <span data-ttu-id="a1fb2-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="a1fb2-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="a1fb2-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1fb2-140">NOTES</span></span>

## <span data-ttu-id="a1fb2-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1fb2-141">RELATED LINKS</span></span>
