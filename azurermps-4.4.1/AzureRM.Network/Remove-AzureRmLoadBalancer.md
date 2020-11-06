---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569288"
---
# <span data-ttu-id="9cfa3-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cfa3-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="9cfa3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cfa3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfa3-103">Удаляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cfa3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cfa3-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cfa3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cfa3-105">DESCRIPTION</span></span>
<span data-ttu-id="9cfa3-106">Командлет **Remove-AzureRmLoadBalancer** Удаляет службу балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="9cfa3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cfa3-107">EXAMPLES</span></span>

### <span data-ttu-id="9cfa3-108">Пример 1: Удаление подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="9cfa3-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9cfa3-109">Эта команда удаляет подсистему балансировки нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="9cfa3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cfa3-110">PARAMETERS</span></span>

### <span data-ttu-id="9cfa3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9cfa3-111">-Force</span></span>
<span data-ttu-id="9cfa3-112">Указывает на то, что этот командлет удаляет подсистему балансировки нагрузки независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cfa3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cfa3-113">-Name</span></span>
<span data-ttu-id="9cfa3-114">Указывает имя подсистемы балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-114">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cfa3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cfa3-115">-PassThru</span></span>
<span data-ttu-id="9cfa3-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cfa3-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cfa3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cfa3-118">-ResourceGroupName</span></span>
<span data-ttu-id="9cfa3-119">Указывает имя группы ресурсов, содержащей подсистему балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cfa3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cfa3-120">-Confirm</span></span>
<span data-ttu-id="9cfa3-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cfa3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cfa3-122">-WhatIf</span></span>
<span data-ttu-id="9cfa3-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cfa3-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cfa3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cfa3-125">-DefaultProfile</span></span>
<span data-ttu-id="9cfa3-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cfa3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfa3-127">CommonParameters</span></span>
<span data-ttu-id="9cfa3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cfa3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfa3-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cfa3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfa3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cfa3-130">INPUTS</span></span>

## <span data-ttu-id="9cfa3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cfa3-131">OUTPUTS</span></span>

## <span data-ttu-id="9cfa3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cfa3-132">NOTES</span></span>

## <span data-ttu-id="9cfa3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cfa3-133">RELATED LINKS</span></span>

[<span data-ttu-id="9cfa3-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cfa3-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9cfa3-135">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cfa3-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="9cfa3-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cfa3-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


