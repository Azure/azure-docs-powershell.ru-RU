---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732199"
---
# <span data-ttu-id="44da4-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="44da4-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="44da4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44da4-102">SYNOPSIS</span></span>
<span data-ttu-id="44da4-103">Обновляет описание WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="44da4-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44da4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44da4-104">SYNTAX</span></span>

### <span data-ttu-id="44da4-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44da4-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44da4-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="44da4-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44da4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44da4-107">DESCRIPTION</span></span>
<span data-ttu-id="44da4-108">Командлет Set-AzureRmWcfRelay обновляет описание для WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="44da4-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="44da4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44da4-109">EXAMPLES</span></span>

### <span data-ttu-id="44da4-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="44da4-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="44da4-111">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="44da4-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="44da4-112">Обновляет указанную WcfRelay с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="44da4-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="44da4-113">В этом примере свойство UserMetadata обновляется новым значением.</span><span class="sxs-lookup"><span data-stu-id="44da4-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="44da4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44da4-114">PARAMETERS</span></span>

### <span data-ttu-id="44da4-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="44da4-115">-UserMetadata</span></span>
<span data-ttu-id="44da4-116">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44da4-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="44da4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44da4-117">-Confirm</span></span>
<span data-ttu-id="44da4-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44da4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44da4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44da4-119">-WhatIf</span></span>
<span data-ttu-id="44da4-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44da4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44da4-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44da4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44da4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44da4-122">-InputObject</span></span>
<span data-ttu-id="44da4-123">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="44da4-123">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44da4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44da4-124">-Name</span></span>
<span data-ttu-id="44da4-125">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="44da4-125">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44da4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="44da4-126">-Namespace</span></span>
<span data-ttu-id="44da4-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="44da4-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44da4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44da4-128">-ResourceGroupName</span></span>
<span data-ttu-id="44da4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44da4-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44da4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44da4-130">-DefaultProfile</span></span>
<span data-ttu-id="44da4-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44da4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44da4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44da4-132">CommonParameters</span></span>
<span data-ttu-id="44da4-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44da4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44da4-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44da4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44da4-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44da4-135">INPUTS</span></span>

### <span data-ttu-id="44da4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44da4-136">-ResourceGroupName</span></span>
<span data-ttu-id="44da4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="44da4-137">System.String</span></span>

### <span data-ttu-id="44da4-138">-+ +</span><span class="sxs-lookup"><span data-stu-id="44da4-138">-NamespaceName</span></span>
<span data-ttu-id="44da4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="44da4-139">System.String</span></span>

### <span data-ttu-id="44da4-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="44da4-140">-WcfRelayName</span></span>
<span data-ttu-id="44da4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="44da4-141">System.String</span></span>

### <span data-ttu-id="44da4-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44da4-142">-InputObject</span></span>
<span data-ttu-id="44da4-143">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="44da4-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="44da4-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="44da4-144">-WcfRelayType</span></span>
<span data-ttu-id="44da4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="44da4-145">System.String</span></span>

### <span data-ttu-id="44da4-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="44da4-146">-UserMetadata</span></span>
<span data-ttu-id="44da4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="44da4-147">System.String</span></span>

## <span data-ttu-id="44da4-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44da4-148">OUTPUTS</span></span>

### <span data-ttu-id="44da4-149">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="44da4-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="44da4-150">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="44da4-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="44da4-151">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="44da4-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="44da4-152">RelayType: HTTP CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true Dynamic: false UserMetadata: UserMetadata — заполнитель для хранения данных, определенных пользователем, для конечной точки HybridConnection. Например: Он может использоваться для хранения данных DESC riptive, таких как список групп и контактные данные, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44da4-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="44da4-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="44da4-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="44da4-154">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="44da4-154">Example 2 - Properties</span></span>

### <span data-ttu-id="44da4-155">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="44da4-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="44da4-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true Dynamic: false UserMetadata: ID метаданных пользователя:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="44da4-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="44da4-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="44da4-157">NOTES</span></span>

## <span data-ttu-id="44da4-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44da4-158">RELATED LINKS</span></span>

