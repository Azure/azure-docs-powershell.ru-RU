---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 872683cbf4e26601ec16f05256f0011b0441127c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733239"
---
# <span data-ttu-id="ea45a-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea45a-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="ea45a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea45a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea45a-103">Удаляет HybridConnection из указанного пространства имен HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="ea45a-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea45a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea45a-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea45a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea45a-105">DESCRIPTION</span></span>
<span data-ttu-id="ea45a-106">Командлет **Remove-AzureRmRelayHybridConnection** удаляет HybridConnection из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="ea45a-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="ea45a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea45a-107">EXAMPLES</span></span>

### <span data-ttu-id="ea45a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea45a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="ea45a-109">Удаляет HybridConnection `TestHybridConnection` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea45a-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ea45a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea45a-110">PARAMETERS</span></span>

### <span data-ttu-id="ea45a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea45a-111">-DefaultProfile</span></span>
<span data-ttu-id="ea45a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea45a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea45a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea45a-113">-Name</span></span>
<span data-ttu-id="ea45a-114">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="ea45a-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ea45a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea45a-115">-Namespace</span></span>
<span data-ttu-id="ea45a-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ea45a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ea45a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea45a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea45a-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea45a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea45a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea45a-119">-Confirm</span></span>
<span data-ttu-id="ea45a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea45a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea45a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea45a-121">-WhatIf</span></span>
<span data-ttu-id="ea45a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea45a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea45a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea45a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea45a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea45a-124">CommonParameters</span></span>
<span data-ttu-id="ea45a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea45a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea45a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea45a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea45a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea45a-127">INPUTS</span></span>

### <span data-ttu-id="ea45a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea45a-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="ea45a-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea45a-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="ea45a-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea45a-130">-Name</span></span>
    System.String

## <span data-ttu-id="ea45a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea45a-131">OUTPUTS</span></span>

### <span data-ttu-id="ea45a-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="ea45a-132">System.Object</span></span>

## <span data-ttu-id="ea45a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea45a-133">NOTES</span></span>

## <span data-ttu-id="ea45a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea45a-134">RELATED LINKS</span></span>

