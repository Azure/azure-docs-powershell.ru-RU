---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242700"
---
# <span data-ttu-id="1fd45-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="1fd45-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="1fd45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fd45-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd45-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd45-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="1fd45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fd45-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd45-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd45-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd45-106">Командлет **Remove-AzRelayNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd45-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="1fd45-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fd45-107">EXAMPLES</span></span>

### <span data-ttu-id="1fd45-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fd45-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="1fd45-109">Удаляет пространство имен ретрансляции `TestNameSpace-Relay1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="1fd45-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="1fd45-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fd45-110">PARAMETERS</span></span>

### <span data-ttu-id="1fd45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd45-111">-DefaultProfile</span></span>
<span data-ttu-id="1fd45-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd45-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd45-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fd45-113">-Name</span></span>
<span data-ttu-id="1fd45-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1fd45-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="1fd45-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd45-115">-ResourceGroupName</span></span>
<span data-ttu-id="1fd45-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd45-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="1fd45-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fd45-117">-Confirm</span></span>
<span data-ttu-id="1fd45-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fd45-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd45-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd45-119">-WhatIf</span></span>
<span data-ttu-id="1fd45-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fd45-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd45-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fd45-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd45-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd45-122">CommonParameters</span></span>
<span data-ttu-id="1fd45-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fd45-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd45-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd45-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd45-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fd45-125">INPUTS</span></span>

### <span data-ttu-id="1fd45-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1fd45-126">System.String</span></span>

## <span data-ttu-id="1fd45-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd45-127">OUTPUTS</span></span>

### <span data-ttu-id="1fd45-128">System. void</span><span class="sxs-lookup"><span data-stu-id="1fd45-128">System.Void</span></span>

## <span data-ttu-id="1fd45-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fd45-129">NOTES</span></span>

## <span data-ttu-id="1fd45-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fd45-130">RELATED LINKS</span></span>
