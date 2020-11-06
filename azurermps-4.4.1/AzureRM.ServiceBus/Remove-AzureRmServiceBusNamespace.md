---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562160"
---
# <span data-ttu-id="9b8a4-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9b8a4-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="9b8a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8a4-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b8a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b8a4-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b8a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8a4-106">Командлет **Remove-AzureRmServiceBusNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="9b8a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8a4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b8a4-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="9b8a4-109">Удаляет пространство имен служебной шины `SB-Example1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="9b8a4-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="9b8a4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b8a4-110">PARAMETERS</span></span>

### <span data-ttu-id="9b8a4-111">-+ +</span><span class="sxs-lookup"><span data-stu-id="9b8a4-111">-NamespaceName</span></span>
<span data-ttu-id="9b8a4-112">Имя пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="9b8a4-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b8a4-113">-ResourceGroup</span></span>
<span data-ttu-id="9b8a4-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b8a4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b8a4-115">-Confirm</span></span>
<span data-ttu-id="9b8a4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8a4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8a4-117">-WhatIf</span></span>
<span data-ttu-id="9b8a4-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8a4-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8a4-120">CommonParameters</span></span>
<span data-ttu-id="9b8a4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b8a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8a4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8a4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b8a4-123">INPUTS</span></span>

### <span data-ttu-id="9b8a4-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b8a4-124">-ResourceGroup</span></span>
 <span data-ttu-id="9b8a4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9b8a4-125">System.String</span></span>

### <span data-ttu-id="9b8a4-126">-+ +</span><span class="sxs-lookup"><span data-stu-id="9b8a4-126">-NamespaceName</span></span>
 <span data-ttu-id="9b8a4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9b8a4-127">System.String</span></span>

## <span data-ttu-id="9b8a4-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b8a4-128">OUTPUTS</span></span>

### <span data-ttu-id="9b8a4-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b8a4-129">System.Object</span></span>

## <span data-ttu-id="9b8a4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b8a4-130">NOTES</span></span>

## <span data-ttu-id="9b8a4-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b8a4-131">RELATED LINKS</span></span>

