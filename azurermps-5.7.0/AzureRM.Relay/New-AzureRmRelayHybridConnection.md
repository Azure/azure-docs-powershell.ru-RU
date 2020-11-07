---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 9398c2229b31e432e55e5c4b11e72d3360b52fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732845"
---
# <span data-ttu-id="51b0c-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="51b0c-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="51b0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="51b0c-103">Создает HybridConnection в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="51b0c-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51b0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51b0c-104">SYNTAX</span></span>

### <span data-ttu-id="51b0c-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="51b0c-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51b0c-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="51b0c-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51b0c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="51b0c-108">Командлет New-AzureRmRelayHybridConnection создает объект HybridConnection в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="51b0c-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="51b0c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="51b0c-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b0c-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

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

<span data-ttu-id="51b0c-111">Создает новый TestHybirdConnection2 HybirdConnection \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="51b0c-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="51b0c-112">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="51b0c-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

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

<span data-ttu-id="51b0c-113">Создает новый TestHybirdConnection1 HybirdConnection \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="51b0c-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="51b0c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51b0c-114">PARAMETERS</span></span>

### <span data-ttu-id="51b0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b0c-115">-DefaultProfile</span></span>
<span data-ttu-id="51b0c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51b0c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51b0c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b0c-117">-InputObject</span></span>
<span data-ttu-id="51b0c-118">Объект HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="51b0c-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b0c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51b0c-119">-Name</span></span>
<span data-ttu-id="51b0c-120">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="51b0c-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b0c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51b0c-121">-Namespace</span></span>
<span data-ttu-id="51b0c-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="51b0c-122">Namespace Name.</span></span>

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

### <span data-ttu-id="51b0c-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="51b0c-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="51b0c-124">значение true, если для этого HybridConnections требуется проверка подлинности клиента; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="51b0c-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b0c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b0c-125">-ResourceGroupName</span></span>
<span data-ttu-id="51b0c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51b0c-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="51b0c-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="51b0c-127">-UserMetadata</span></span>
<span data-ttu-id="51b0c-128">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="51b0c-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b0c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51b0c-129">-Confirm</span></span>
<span data-ttu-id="51b0c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51b0c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b0c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b0c-131">-WhatIf</span></span>
<span data-ttu-id="51b0c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51b0c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b0c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51b0c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b0c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b0c-134">CommonParameters</span></span>
<span data-ttu-id="51b0c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51b0c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b0c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b0c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b0c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51b0c-137">INPUTS</span></span>

### <span data-ttu-id="51b0c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b0c-138">-ResourceGroupName</span></span>
<span data-ttu-id="51b0c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="51b0c-139">System.String</span></span>

### <span data-ttu-id="51b0c-140">-+ +</span><span class="sxs-lookup"><span data-stu-id="51b0c-140">-NamespaceName</span></span>
<span data-ttu-id="51b0c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="51b0c-141">System.String</span></span>

### <span data-ttu-id="51b0c-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="51b0c-142">-HybridConnectionsName</span></span>
<span data-ttu-id="51b0c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51b0c-143">System.String</span></span>

### <span data-ttu-id="51b0c-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b0c-144">-InputObject</span></span>
<span data-ttu-id="51b0c-145">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="51b0c-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="51b0c-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="51b0c-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="51b0c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51b0c-147">System.Boolean</span></span>

### <span data-ttu-id="51b0c-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="51b0c-148">-UserMetadata</span></span>
<span data-ttu-id="51b0c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="51b0c-149">System.String</span></span>

## <span data-ttu-id="51b0c-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51b0c-150">OUTPUTS</span></span>

### <span data-ttu-id="51b0c-151">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="51b0c-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="51b0c-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="51b0c-152">NOTES</span></span>

## <span data-ttu-id="51b0c-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51b0c-153">RELATED LINKS</span></span>

