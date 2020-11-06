---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568313"
---
# <span data-ttu-id="eee87-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="eee87-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="eee87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eee87-102">SYNOPSIS</span></span>
<span data-ttu-id="eee87-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee87-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eee87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eee87-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee87-105">DESCRIPTION</span></span>
<span data-ttu-id="eee87-106">Командлет **Remove-AzureRmRelayNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee87-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="eee87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eee87-107">EXAMPLES</span></span>

### <span data-ttu-id="eee87-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eee87-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="eee87-109">Удаляет пространство имен ретрансляции `TestNameSpace-Relay1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="eee87-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="eee87-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eee87-110">PARAMETERS</span></span>

### <span data-ttu-id="eee87-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eee87-111">-Name</span></span>
<span data-ttu-id="eee87-112">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="eee87-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="eee87-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee87-113">-ResourceGroupName</span></span>
<span data-ttu-id="eee87-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee87-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="eee87-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eee87-115">-Confirm</span></span>
<span data-ttu-id="eee87-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eee87-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee87-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee87-117">-WhatIf</span></span>
<span data-ttu-id="eee87-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eee87-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee87-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eee87-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee87-120">-DefaultProfile</span></span>
<span data-ttu-id="eee87-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eee87-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee87-122">CommonParameters</span></span>
<span data-ttu-id="eee87-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eee87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee87-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee87-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee87-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eee87-125">INPUTS</span></span>

### <span data-ttu-id="eee87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee87-126">-ResourceGroupName</span></span>
 <span data-ttu-id="eee87-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eee87-127">System.String</span></span>

### <span data-ttu-id="eee87-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eee87-128">-Name</span></span>
 <span data-ttu-id="eee87-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eee87-129">System.String</span></span>

## <span data-ttu-id="eee87-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee87-130">OUTPUTS</span></span>

### <span data-ttu-id="eee87-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="eee87-131">System.Object</span></span>

## <span data-ttu-id="eee87-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="eee87-132">NOTES</span></span>

## <span data-ttu-id="eee87-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eee87-133">RELATED LINKS</span></span>

