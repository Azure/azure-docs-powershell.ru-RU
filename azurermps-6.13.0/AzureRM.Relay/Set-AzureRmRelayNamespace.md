---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732292"
---
# <span data-ttu-id="71402-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="71402-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="71402-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71402-102">SYNOPSIS</span></span>
<span data-ttu-id="71402-103">Обновляет описание существующего пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="71402-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71402-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71402-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71402-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71402-105">DESCRIPTION</span></span>
<span data-ttu-id="71402-106">Командлет **Set-AzureRmRelayNamespace** обновляет описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71402-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="71402-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71402-107">EXAMPLES</span></span>

### <span data-ttu-id="71402-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71402-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="71402-109">Обновляет пространство имен ретрансляции с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="71402-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="71402-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71402-110">PARAMETERS</span></span>

### <span data-ttu-id="71402-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71402-111">-DefaultProfile</span></span>
<span data-ttu-id="71402-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71402-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71402-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71402-113">-InputObject</span></span>
<span data-ttu-id="71402-114">Объект пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="71402-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="71402-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71402-115">-Name</span></span>
<span data-ttu-id="71402-116">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="71402-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="71402-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71402-117">-ResourceGroupName</span></span>
<span data-ttu-id="71402-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71402-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="71402-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="71402-119">-Tag</span></span>
<span data-ttu-id="71402-120">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="71402-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="71402-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71402-121">-Confirm</span></span>
<span data-ttu-id="71402-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71402-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71402-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71402-123">-WhatIf</span></span>
<span data-ttu-id="71402-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71402-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71402-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71402-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71402-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71402-126">CommonParameters</span></span>
<span data-ttu-id="71402-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71402-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="71402-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71402-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71402-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71402-129">INPUTS</span></span>

### <span data-ttu-id="71402-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71402-130">System.String</span></span>
<span data-ttu-id="71402-131">System. Collections. Hashtable Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="71402-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="71402-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71402-132">OUTPUTS</span></span>

### <span data-ttu-id="71402-133">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="71402-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="71402-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="71402-134">NOTES</span></span>

## <span data-ttu-id="71402-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71402-135">RELATED LINKS</span></span>
