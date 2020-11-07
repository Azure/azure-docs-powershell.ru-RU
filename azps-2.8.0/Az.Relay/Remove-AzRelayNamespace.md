---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: dec858fe113725876e7e46d72cf996d9338b34eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905678"
---
# <span data-ttu-id="e14da-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="e14da-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="e14da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e14da-102">SYNOPSIS</span></span>
<span data-ttu-id="e14da-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e14da-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="e14da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e14da-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e14da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e14da-105">DESCRIPTION</span></span>
<span data-ttu-id="e14da-106">Командлет **Remove-AzRelayNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e14da-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="e14da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e14da-107">EXAMPLES</span></span>

### <span data-ttu-id="e14da-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e14da-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="e14da-109">Удаляет пространство имен ретрансляции `TestNameSpace-Relay1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="e14da-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="e14da-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e14da-110">PARAMETERS</span></span>

### <span data-ttu-id="e14da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14da-111">-DefaultProfile</span></span>
<span data-ttu-id="e14da-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e14da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14da-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e14da-113">-Name</span></span>
<span data-ttu-id="e14da-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e14da-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="e14da-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14da-115">-ResourceGroupName</span></span>
<span data-ttu-id="e14da-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e14da-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="e14da-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e14da-117">-Confirm</span></span>
<span data-ttu-id="e14da-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e14da-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e14da-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14da-119">-WhatIf</span></span>
<span data-ttu-id="e14da-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e14da-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e14da-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e14da-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e14da-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14da-122">CommonParameters</span></span>
<span data-ttu-id="e14da-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e14da-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14da-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e14da-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14da-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e14da-125">INPUTS</span></span>

### <span data-ttu-id="e14da-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e14da-126">System.String</span></span>

## <span data-ttu-id="e14da-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e14da-127">OUTPUTS</span></span>

### <span data-ttu-id="e14da-128">System. void</span><span class="sxs-lookup"><span data-stu-id="e14da-128">System.Void</span></span>

## <span data-ttu-id="e14da-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e14da-129">NOTES</span></span>

## <span data-ttu-id="e14da-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e14da-130">RELATED LINKS</span></span>
