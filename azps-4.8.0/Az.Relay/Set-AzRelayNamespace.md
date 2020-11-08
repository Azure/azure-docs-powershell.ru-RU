---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077671"
---
# <span data-ttu-id="3ca9b-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="3ca9b-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="3ca9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ca9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca9b-103">Обновляет описание существующего пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="3ca9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ca9b-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ca9b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ca9b-106">Командлет **Set-AzRelayNamespace** обновляет описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="3ca9b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ca9b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ca9b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ca9b-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="3ca9b-109">Обновляет пространство имен ретрансляции с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="3ca9b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ca9b-110">PARAMETERS</span></span>

### <span data-ttu-id="3ca9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca9b-111">-DefaultProfile</span></span>
<span data-ttu-id="3ca9b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca9b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca9b-113">-InputObject</span></span>
<span data-ttu-id="3ca9b-114">Объект пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca9b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ca9b-115">-Name</span></span>
<span data-ttu-id="3ca9b-116">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="3ca9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ca9b-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ca9b-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="3ca9b-119">-Tag</span></span>
<span data-ttu-id="3ca9b-120">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-120">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca9b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ca9b-121">-Confirm</span></span>
<span data-ttu-id="3ca9b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca9b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca9b-123">-WhatIf</span></span>
<span data-ttu-id="3ca9b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca9b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca9b-126">CommonParameters</span></span>
<span data-ttu-id="3ca9b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ca9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca9b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca9b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca9b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ca9b-129">INPUTS</span></span>

### <span data-ttu-id="3ca9b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca9b-130">System.String</span></span>

### <span data-ttu-id="3ca9b-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ca9b-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3ca9b-132">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="3ca9b-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="3ca9b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ca9b-133">OUTPUTS</span></span>

### <span data-ttu-id="3ca9b-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3ca9b-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="3ca9b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ca9b-135">NOTES</span></span>

## <span data-ttu-id="3ca9b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ca9b-136">RELATED LINKS</span></span>
