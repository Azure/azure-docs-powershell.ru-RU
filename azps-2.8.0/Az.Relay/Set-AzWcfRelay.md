---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905665"
---
# <span data-ttu-id="d0991-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="d0991-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="d0991-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0991-102">SYNOPSIS</span></span>
<span data-ttu-id="d0991-103">Обновляет описание WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="d0991-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="d0991-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0991-104">SYNTAX</span></span>

### <span data-ttu-id="d0991-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0991-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0991-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d0991-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0991-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0991-107">DESCRIPTION</span></span>
<span data-ttu-id="d0991-108">Командлет Set-AzWcfRelay обновляет описание для WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="d0991-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="d0991-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0991-109">EXAMPLES</span></span>

### <span data-ttu-id="d0991-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0991-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="d0991-111">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="d0991-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="d0991-112">Обновляет указанную WcfRelay с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d0991-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="d0991-113">В этом примере свойство UserMetadata обновляется новым значением.</span><span class="sxs-lookup"><span data-stu-id="d0991-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="d0991-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0991-114">PARAMETERS</span></span>

### <span data-ttu-id="d0991-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0991-115">-DefaultProfile</span></span>
<span data-ttu-id="d0991-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0991-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0991-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0991-117">-InputObject</span></span>
<span data-ttu-id="d0991-118">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="d0991-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="d0991-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0991-119">-Name</span></span>
<span data-ttu-id="d0991-120">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="d0991-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d0991-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0991-121">-Namespace</span></span>
<span data-ttu-id="d0991-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d0991-122">Namespace Name.</span></span>

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

### <span data-ttu-id="d0991-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0991-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0991-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0991-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0991-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d0991-125">-UserMetadata</span></span>
<span data-ttu-id="d0991-126">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки WcfRelay. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d0991-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="d0991-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0991-127">-Confirm</span></span>
<span data-ttu-id="d0991-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0991-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0991-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0991-129">-WhatIf</span></span>
<span data-ttu-id="d0991-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0991-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0991-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0991-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0991-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0991-132">CommonParameters</span></span>
<span data-ttu-id="d0991-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0991-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0991-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0991-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0991-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0991-135">INPUTS</span></span>

### <span data-ttu-id="d0991-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d0991-136">System.String</span></span>

### <span data-ttu-id="d0991-137">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="d0991-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="d0991-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0991-138">OUTPUTS</span></span>

### <span data-ttu-id="d0991-139">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="d0991-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="d0991-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0991-140">NOTES</span></span>

## <span data-ttu-id="d0991-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0991-141">RELATED LINKS</span></span>
