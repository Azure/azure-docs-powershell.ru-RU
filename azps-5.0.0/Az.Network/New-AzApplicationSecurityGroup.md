---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248559"
---
# <span data-ttu-id="35bf5-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35bf5-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="35bf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="35bf5-103">Создание группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="35bf5-103">Creates an application security group.</span></span>

## <span data-ttu-id="35bf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35bf5-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35bf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="35bf5-106">Командлет **New-AzApplicationSecurityGroup** создает группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="35bf5-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="35bf5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="35bf5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35bf5-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="35bf5-109">В этом примере создается группа безопасности приложения без ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="35bf5-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="35bf5-110">После создания IP-конфигурации в сетевом интерфейсе можно включить в группу.</span><span class="sxs-lookup"><span data-stu-id="35bf5-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="35bf5-111">Правила безопасности могут также ссылаться на группу в качестве источников или назначений.</span><span class="sxs-lookup"><span data-stu-id="35bf5-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="35bf5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35bf5-112">PARAMETERS</span></span>

### <span data-ttu-id="35bf5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35bf5-113">-AsJob</span></span>
<span data-ttu-id="35bf5-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35bf5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35bf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35bf5-115">-DefaultProfile</span></span>
<span data-ttu-id="35bf5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35bf5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35bf5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="35bf5-117">-Force</span></span>
<span data-ttu-id="35bf5-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс.</span><span class="sxs-lookup"><span data-stu-id="35bf5-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="35bf5-119">-Location</span><span class="sxs-lookup"><span data-stu-id="35bf5-119">-Location</span></span>
<span data-ttu-id="35bf5-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="35bf5-120">The location.</span></span>

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

### <span data-ttu-id="35bf5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35bf5-121">-Name</span></span>
<span data-ttu-id="35bf5-122">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="35bf5-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="35bf5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35bf5-123">-ResourceGroupName</span></span>
<span data-ttu-id="35bf5-124">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="35bf5-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="35bf5-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="35bf5-125">-Tag</span></span>
<span data-ttu-id="35bf5-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35bf5-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="35bf5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35bf5-127">-Confirm</span></span>
<span data-ttu-id="35bf5-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35bf5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35bf5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35bf5-129">-WhatIf</span></span>
<span data-ttu-id="35bf5-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35bf5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35bf5-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35bf5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35bf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35bf5-132">CommonParameters</span></span>
<span data-ttu-id="35bf5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35bf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35bf5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35bf5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35bf5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35bf5-135">INPUTS</span></span>

### <span data-ttu-id="35bf5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="35bf5-136">System.String</span></span>

### <span data-ttu-id="35bf5-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35bf5-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="35bf5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35bf5-138">OUTPUTS</span></span>

### <span data-ttu-id="35bf5-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35bf5-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="35bf5-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="35bf5-140">NOTES</span></span>

## <span data-ttu-id="35bf5-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35bf5-141">RELATED LINKS</span></span>

[<span data-ttu-id="35bf5-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35bf5-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="35bf5-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35bf5-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="35bf5-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35bf5-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="35bf5-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35bf5-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="35bf5-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35bf5-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="35bf5-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="35bf5-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="35bf5-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="35bf5-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="35bf5-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="35bf5-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
