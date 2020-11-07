---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732837"
---
# <span data-ttu-id="e32f7-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e32f7-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="e32f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e32f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e32f7-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e32f7-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e32f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e32f7-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e32f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e32f7-106">Командлет **Remove-AzureRmServiceBusNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e32f7-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="e32f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e32f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e32f7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e32f7-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="e32f7-109">Удаляет пространство имен служебной шины `SB-Example1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="e32f7-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="e32f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e32f7-110">PARAMETERS</span></span>

### <span data-ttu-id="e32f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32f7-111">-DefaultProfile</span></span>
<span data-ttu-id="e32f7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e32f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e32f7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e32f7-113">-Name</span></span>
<span data-ttu-id="e32f7-114">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e32f7-114">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e32f7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e32f7-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32f7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e32f7-117">-Confirm</span></span>
<span data-ttu-id="e32f7-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e32f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e32f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32f7-119">-WhatIf</span></span>
<span data-ttu-id="e32f7-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e32f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e32f7-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e32f7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e32f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32f7-122">CommonParameters</span></span>
<span data-ttu-id="e32f7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e32f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32f7-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32f7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e32f7-125">INPUTS</span></span>

### <span data-ttu-id="e32f7-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e32f7-126">-ResourceGroup</span></span>
 <span data-ttu-id="e32f7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e32f7-127">System.String</span></span>

### <span data-ttu-id="e32f7-128">-+ +</span><span class="sxs-lookup"><span data-stu-id="e32f7-128">-NamespaceName</span></span>
 <span data-ttu-id="e32f7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e32f7-129">System.String</span></span>

## <span data-ttu-id="e32f7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e32f7-130">OUTPUTS</span></span>

### <span data-ttu-id="e32f7-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="e32f7-131">System.Object</span></span>

## <span data-ttu-id="e32f7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e32f7-132">NOTES</span></span>

## <span data-ttu-id="e32f7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e32f7-133">RELATED LINKS</span></span>

