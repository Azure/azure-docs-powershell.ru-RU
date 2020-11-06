---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561559"
---
# <span data-ttu-id="dce8e-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="dce8e-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="dce8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dce8e-102">SYNOPSIS</span></span>
<span data-ttu-id="dce8e-103">Обновляет описание WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="dce8e-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dce8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dce8e-104">SYNTAX</span></span>

### <span data-ttu-id="dce8e-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dce8e-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dce8e-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dce8e-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dce8e-107">DESCRIPTION</span></span>
<span data-ttu-id="dce8e-108">Командлет Set-AzureRmWcfRelay обновляет описание для WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="dce8e-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="dce8e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dce8e-109">EXAMPLES</span></span>

### <span data-ttu-id="dce8e-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8e-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="dce8e-111">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="dce8e-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="dce8e-112">Обновляет указанную WcfRelay с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="dce8e-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="dce8e-113">В этом примере свойство UserMetadata обновляется новым значением.</span><span class="sxs-lookup"><span data-stu-id="dce8e-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="dce8e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dce8e-114">PARAMETERS</span></span>

### <span data-ttu-id="dce8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce8e-115">-DefaultProfile</span></span>
<span data-ttu-id="dce8e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dce8e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dce8e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8e-117">-InputObject</span></span>
<span data-ttu-id="dce8e-118">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dce8e-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dce8e-119">-Name</span></span>
<span data-ttu-id="dce8e-120">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="dce8e-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dce8e-121">-Namespace</span></span>
<span data-ttu-id="dce8e-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dce8e-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="dce8e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dce8e-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="dce8e-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="dce8e-125">-UserMetadata</span></span>
<span data-ttu-id="dce8e-126">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dce8e-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dce8e-127">-Confirm</span></span>
<span data-ttu-id="dce8e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dce8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce8e-129">-WhatIf</span></span>
<span data-ttu-id="dce8e-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dce8e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce8e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dce8e-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce8e-132">CommonParameters</span></span>
<span data-ttu-id="dce8e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dce8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce8e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce8e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce8e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dce8e-135">INPUTS</span></span>

### <span data-ttu-id="dce8e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce8e-136">-ResourceGroupName</span></span>
<span data-ttu-id="dce8e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dce8e-137">System.String</span></span>

### <span data-ttu-id="dce8e-138">-+ +</span><span class="sxs-lookup"><span data-stu-id="dce8e-138">-NamespaceName</span></span>
<span data-ttu-id="dce8e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dce8e-139">System.String</span></span>

### <span data-ttu-id="dce8e-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="dce8e-140">-WcfRelayName</span></span>
<span data-ttu-id="dce8e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dce8e-141">System.String</span></span>

### <span data-ttu-id="dce8e-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8e-142">-InputObject</span></span>
<span data-ttu-id="dce8e-143">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dce8e-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="dce8e-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="dce8e-144">-WcfRelayType</span></span>
<span data-ttu-id="dce8e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dce8e-145">System.String</span></span>

### <span data-ttu-id="dce8e-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="dce8e-146">-UserMetadata</span></span>
<span data-ttu-id="dce8e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="dce8e-147">System.String</span></span>

## <span data-ttu-id="dce8e-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dce8e-148">OUTPUTS</span></span>

### <span data-ttu-id="dce8e-149">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dce8e-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="dce8e-150">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8e-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="dce8e-151">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dce8e-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="dce8e-152">RelayType: HTTP CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true Dynamic: false UserMetadata: UserMetadata — заполнитель для хранения данных, определенных пользователем, для конечной точки HybridConnection. Например: Он может использоваться для хранения данных DESC riptive, таких как список групп и контактные данные, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dce8e-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="dce8e-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="dce8e-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="dce8e-154">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="dce8e-154">Example 2 - Properties</span></span>

### <span data-ttu-id="dce8e-155">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dce8e-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="dce8e-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true Dynamic: false UserMetadata: ID метаданных пользователя:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="dce8e-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="dce8e-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="dce8e-157">NOTES</span></span>

## <span data-ttu-id="dce8e-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dce8e-158">RELATED LINKS</span></span>

