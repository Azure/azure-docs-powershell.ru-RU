---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912755"
---
# <span data-ttu-id="2a190-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="2a190-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="2a190-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a190-102">SYNOPSIS</span></span>
<span data-ttu-id="2a190-103">Создает HybridConnection в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="2a190-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="2a190-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a190-104">SYNTAX</span></span>

### <span data-ttu-id="2a190-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a190-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a190-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2a190-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a190-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a190-107">DESCRIPTION</span></span>
<span data-ttu-id="2a190-108">Командлет New-AzRelayHybridConnection создает объект HybridConnection в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="2a190-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="2a190-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a190-109">EXAMPLES</span></span>

### <span data-ttu-id="2a190-110">Пример 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a190-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="2a190-111">Создает новый TestHybirdConnection2 HybirdConnection \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="2a190-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="2a190-112">Пример 2: свойства</span><span class="sxs-lookup"><span data-stu-id="2a190-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="2a190-113">Создает новый TestHybirdConnection1 HybirdConnection \` \` в указанном пространстве имен ретрансляции \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="2a190-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="2a190-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a190-114">PARAMETERS</span></span>

### <span data-ttu-id="2a190-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a190-115">-DefaultProfile</span></span>
<span data-ttu-id="2a190-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a190-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a190-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a190-117">-InputObject</span></span>
<span data-ttu-id="2a190-118">Объект HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="2a190-118">HybridConnections object.</span></span>

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

### <span data-ttu-id="2a190-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a190-119">-Name</span></span>
<span data-ttu-id="2a190-120">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="2a190-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="2a190-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2a190-121">-Namespace</span></span>
<span data-ttu-id="2a190-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2a190-122">Namespace Name.</span></span>

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

### <span data-ttu-id="2a190-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="2a190-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="2a190-124">значение true, если для этого HybridConnections требуется проверка подлинности клиента; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="2a190-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="2a190-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a190-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a190-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a190-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="2a190-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="2a190-127">-UserMetadata</span></span>
<span data-ttu-id="2a190-128">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2a190-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="2a190-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a190-129">-Confirm</span></span>
<span data-ttu-id="2a190-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a190-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a190-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a190-131">-WhatIf</span></span>
<span data-ttu-id="2a190-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a190-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a190-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a190-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a190-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a190-134">CommonParameters</span></span>
<span data-ttu-id="2a190-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a190-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a190-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a190-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a190-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a190-137">INPUTS</span></span>

### <span data-ttu-id="2a190-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2a190-138">System.String</span></span>

### <span data-ttu-id="2a190-139">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="2a190-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="2a190-140">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2a190-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2a190-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a190-141">OUTPUTS</span></span>

### <span data-ttu-id="2a190-142">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="2a190-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="2a190-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a190-143">NOTES</span></span>

## <span data-ttu-id="2a190-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a190-144">RELATED LINKS</span></span>
