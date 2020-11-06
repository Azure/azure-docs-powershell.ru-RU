---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558303"
---
# <span data-ttu-id="52bc6-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="52bc6-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="52bc6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="52bc6-103">Создает WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="52bc6-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52bc6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52bc6-104">SYNTAX</span></span>

### <span data-ttu-id="52bc6-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="52bc6-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52bc6-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="52bc6-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52bc6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52bc6-107">DESCRIPTION</span></span>
<span data-ttu-id="52bc6-108">Командлет New-AzureRmWcfRelay создает объект WcfRelay в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="52bc6-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="52bc6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52bc6-109">EXAMPLES</span></span>

### <span data-ttu-id="52bc6-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="52bc6-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

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

<span data-ttu-id="52bc6-111">Создает новый TestWCFRelay2 WcfRelay \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="52bc6-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="52bc6-112">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="52bc6-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

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

<span data-ttu-id="52bc6-113">Создает новый TestWCFRelay WcfRelay \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="52bc6-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="52bc6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52bc6-114">PARAMETERS</span></span>

### <span data-ttu-id="52bc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bc6-115">-DefaultProfile</span></span>
<span data-ttu-id="52bc6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52bc6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52bc6-117">-InputObject</span></span>
<span data-ttu-id="52bc6-118">Объект WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="52bc6-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="52bc6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52bc6-119">-Name</span></span>
<span data-ttu-id="52bc6-120">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="52bc6-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="52bc6-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="52bc6-121">-Namespace</span></span>
<span data-ttu-id="52bc6-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="52bc6-122">Namespace Name.</span></span>

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

### <span data-ttu-id="52bc6-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="52bc6-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="52bc6-124">значение true, если для этого ретранслятора требуется проверка подлинности клиента; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="52bc6-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="52bc6-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="52bc6-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="52bc6-126">значение true, если для этого ретранслятора требуется безопасность транспорта; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="52bc6-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="52bc6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52bc6-127">-ResourceGroupName</span></span>
<span data-ttu-id="52bc6-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52bc6-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="52bc6-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="52bc6-129">-UserMetadata</span></span>
<span data-ttu-id="52bc6-130">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="52bc6-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="52bc6-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="52bc6-131">-WcfRelayType</span></span>
<span data-ttu-id="52bc6-132">Тип WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="52bc6-132">WcfRelay Type.</span></span>
<span data-ttu-id="52bc6-133">Возможные значения: "NetTcp" или "http"</span><span class="sxs-lookup"><span data-stu-id="52bc6-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="52bc6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52bc6-134">-Confirm</span></span>
<span data-ttu-id="52bc6-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52bc6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52bc6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52bc6-136">-WhatIf</span></span>
<span data-ttu-id="52bc6-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52bc6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52bc6-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52bc6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52bc6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bc6-139">CommonParameters</span></span>
<span data-ttu-id="52bc6-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52bc6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="52bc6-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52bc6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bc6-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52bc6-142">INPUTS</span></span>

### <span data-ttu-id="52bc6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="52bc6-143">System.String</span></span>
<span data-ttu-id="52bc6-144">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="52bc6-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="52bc6-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52bc6-145">OUTPUTS</span></span>

### <span data-ttu-id="52bc6-146">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="52bc6-146">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="52bc6-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="52bc6-147">NOTES</span></span>

## <span data-ttu-id="52bc6-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52bc6-148">RELATED LINKS</span></span>
