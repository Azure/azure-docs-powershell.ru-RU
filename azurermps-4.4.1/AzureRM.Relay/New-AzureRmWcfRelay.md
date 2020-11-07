---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733633"
---
# <span data-ttu-id="8c5f7-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="8c5f7-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="8c5f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5f7-103">Создает WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c5f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c5f7-104">SYNTAX</span></span>

### <span data-ttu-id="8c5f7-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c5f7-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c5f7-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8c5f7-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c5f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c5f7-107">DESCRIPTION</span></span>
<span data-ttu-id="8c5f7-108">Командлет New-AzureRmWcfRelay создает объект WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="8c5f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c5f7-109">EXAMPLES</span></span>

### <span data-ttu-id="8c5f7-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5f7-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="8c5f7-111">Создает новый TestWCFRelay2 WcfRelay \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="8c5f7-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="8c5f7-112">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="8c5f7-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="8c5f7-113">Создает новый TestWCFRelay WcfRelay \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="8c5f7-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="8c5f7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c5f7-114">PARAMETERS</span></span>

### <span data-ttu-id="8c5f7-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="8c5f7-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="8c5f7-116">значение true, если для этого ретранслятора требуется проверка подлинности клиента; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-116">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="8c5f7-117">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5f7-117">-RequiresTransportSecurity</span></span>
<span data-ttu-id="8c5f7-118">значение true, если для этого ретранслятора требуется безопасность транспорта; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-118">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="8c5f7-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8c5f7-119">-UserMetadata</span></span>
<span data-ttu-id="8c5f7-120">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-120">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="8c5f7-121">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="8c5f7-121">-WcfRelayType</span></span>
<span data-ttu-id="8c5f7-122">Тип WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-122">WcfRelay Type.</span></span>
<span data-ttu-id="8c5f7-123">Возможные значения: "NetTcp" или "http"</span><span class="sxs-lookup"><span data-stu-id="8c5f7-123">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="8c5f7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c5f7-124">-Confirm</span></span>
<span data-ttu-id="8c5f7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c5f7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c5f7-126">-WhatIf</span></span>
<span data-ttu-id="8c5f7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c5f7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c5f7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5f7-129">-InputObject</span></span>
<span data-ttu-id="8c5f7-130">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-130">WcfRelay object.</span></span>

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

### <span data-ttu-id="8c5f7-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c5f7-131">-Name</span></span>
<span data-ttu-id="8c5f7-132">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-132">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8c5f7-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c5f7-133">-Namespace</span></span>
<span data-ttu-id="8c5f7-134">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-134">Namespace Name.</span></span>

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

### <span data-ttu-id="8c5f7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c5f7-135">-ResourceGroupName</span></span>
<span data-ttu-id="8c5f7-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c5f7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c5f7-137">-DefaultProfile</span></span>
<span data-ttu-id="8c5f7-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c5f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5f7-139">CommonParameters</span></span>
<span data-ttu-id="8c5f7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c5f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5f7-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c5f7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5f7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c5f7-142">INPUTS</span></span>

### <span data-ttu-id="8c5f7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c5f7-143">-ResourceGroupName</span></span>
<span data-ttu-id="8c5f7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5f7-144">System.String</span></span>

### <span data-ttu-id="8c5f7-145">-+ +</span><span class="sxs-lookup"><span data-stu-id="8c5f7-145">-NamespaceName</span></span>
<span data-ttu-id="8c5f7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5f7-146">System.String</span></span>

### <span data-ttu-id="8c5f7-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="8c5f7-147">-WcfRelayName</span></span>
<span data-ttu-id="8c5f7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5f7-148">System.String</span></span>

### <span data-ttu-id="8c5f7-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5f7-149">-InputObject</span></span>
<span data-ttu-id="8c5f7-150">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="8c5f7-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="8c5f7-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="8c5f7-151">-WcfRelayType</span></span>
<span data-ttu-id="8c5f7-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5f7-152">System.String</span></span>

### <span data-ttu-id="8c5f7-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="8c5f7-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="8c5f7-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c5f7-154">System.Boolean</span></span>

### <span data-ttu-id="8c5f7-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5f7-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="8c5f7-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c5f7-156">System.Boolean</span></span>

### <span data-ttu-id="8c5f7-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8c5f7-157">-UserMetadata</span></span>
<span data-ttu-id="8c5f7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5f7-158">System.String</span></span>

## <span data-ttu-id="8c5f7-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c5f7-159">OUTPUTS</span></span>

### <span data-ttu-id="8c5f7-160">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5f7-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="8c5f7-161">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="8c5f7-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="8c5f7-162">RelayType: HTTP CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true Dynamic: false UserMetadata: TestWCFRelay2 ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="8c5f7-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="8c5f7-163">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="8c5f7-163">Example 2 - Properties</span></span>

### <span data-ttu-id="8c5f7-164">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="8c5f7-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="8c5f7-165">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true Dynamic: false UserMetadata: ID метаданных пользователя:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="8c5f7-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="8c5f7-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c5f7-166">NOTES</span></span>

## <span data-ttu-id="8c5f7-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c5f7-167">RELATED LINKS</span></span>

