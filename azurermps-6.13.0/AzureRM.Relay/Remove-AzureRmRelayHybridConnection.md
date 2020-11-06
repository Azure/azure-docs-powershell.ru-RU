---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 746033cfdf48782d10c0fdabf7a018d309269afb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556519"
---
# <span data-ttu-id="66a1d-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="66a1d-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="66a1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="66a1d-103">Удаляет HybridConnection из указанного пространства имен HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="66a1d-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66a1d-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a1d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="66a1d-106">Командлет **Remove-AzureRmRelayHybridConnection** удаляет HybridConnection из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="66a1d-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="66a1d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66a1d-107">EXAMPLES</span></span>

### <span data-ttu-id="66a1d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66a1d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="66a1d-109">Удаляет HybridConnection `TestHybridConnection` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="66a1d-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="66a1d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66a1d-110">PARAMETERS</span></span>

### <span data-ttu-id="66a1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a1d-111">-DefaultProfile</span></span>
<span data-ttu-id="66a1d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66a1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a1d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66a1d-113">-Name</span></span>
<span data-ttu-id="66a1d-114">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="66a1d-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="66a1d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66a1d-115">-Namespace</span></span>
<span data-ttu-id="66a1d-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="66a1d-116">Namespace Name.</span></span>

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

### <span data-ttu-id="66a1d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a1d-117">-ResourceGroupName</span></span>
<span data-ttu-id="66a1d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66a1d-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="66a1d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66a1d-119">-Confirm</span></span>
<span data-ttu-id="66a1d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66a1d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a1d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a1d-121">-WhatIf</span></span>
<span data-ttu-id="66a1d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66a1d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a1d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66a1d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a1d-124">CommonParameters</span></span>
<span data-ttu-id="66a1d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66a1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66a1d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a1d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a1d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66a1d-127">INPUTS</span></span>

### <span data-ttu-id="66a1d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="66a1d-128">System.String</span></span>


## <span data-ttu-id="66a1d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66a1d-129">OUTPUTS</span></span>

### <span data-ttu-id="66a1d-130">System. void</span><span class="sxs-lookup"><span data-stu-id="66a1d-130">System.Void</span></span>


## <span data-ttu-id="66a1d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="66a1d-131">NOTES</span></span>

## <span data-ttu-id="66a1d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66a1d-132">RELATED LINKS</span></span>
