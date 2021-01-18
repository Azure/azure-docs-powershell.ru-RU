---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505547"
---
# <span data-ttu-id="b1042-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1042-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b1042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1042-102">SYNOPSIS</span></span>
<span data-ttu-id="b1042-103">Создает группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="b1042-103">Creates an application security group.</span></span>

## <span data-ttu-id="b1042-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1042-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1042-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1042-105">DESCRIPTION</span></span>
<span data-ttu-id="b1042-106">Для создания группы безопасности приложений создается группа безопасности **New-AzApplicationSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="b1042-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="b1042-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1042-107">EXAMPLES</span></span>

### <span data-ttu-id="b1042-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1042-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="b1042-109">В этом примере создается группа безопасности приложений без каких-либо связи.</span><span class="sxs-lookup"><span data-stu-id="b1042-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="b1042-110">После создания конфигурации IP-адреса в сетевом интерфейсе можно включить в группу.</span><span class="sxs-lookup"><span data-stu-id="b1042-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="b1042-111">Правила безопасности также могут ссылаться на группу в качестве источников или назначений.</span><span class="sxs-lookup"><span data-stu-id="b1042-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="b1042-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1042-112">PARAMETERS</span></span>

### <span data-ttu-id="b1042-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1042-113">-AsJob</span></span>
<span data-ttu-id="b1042-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b1042-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1042-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1042-115">-DefaultProfile</span></span>
<span data-ttu-id="b1042-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1042-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1042-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b1042-117">-Force</span></span>
<span data-ttu-id="b1042-118">Не спрашивайте подтверждения, если вы хотите переписать ресурс.</span><span class="sxs-lookup"><span data-stu-id="b1042-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="b1042-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b1042-119">-Location</span></span>
<span data-ttu-id="b1042-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="b1042-120">The location.</span></span>

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

### <span data-ttu-id="b1042-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1042-121">-Name</span></span>
<span data-ttu-id="b1042-122">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="b1042-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="b1042-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1042-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1042-124">Имя группы ресурсов группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="b1042-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b1042-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1042-125">-Tag</span></span>
<span data-ttu-id="b1042-126">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="b1042-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b1042-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1042-127">-Confirm</span></span>
<span data-ttu-id="b1042-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1042-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1042-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1042-129">-WhatIf</span></span>
<span data-ttu-id="b1042-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1042-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1042-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1042-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1042-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1042-132">CommonParameters</span></span>
<span data-ttu-id="b1042-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1042-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1042-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1042-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1042-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1042-135">INPUTS</span></span>

### <span data-ttu-id="b1042-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b1042-136">System.String</span></span>

### <span data-ttu-id="b1042-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1042-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1042-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1042-138">OUTPUTS</span></span>

### <span data-ttu-id="b1042-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1042-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="b1042-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1042-140">NOTES</span></span>

## <span data-ttu-id="b1042-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1042-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1042-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1042-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b1042-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1042-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b1042-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1042-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b1042-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1042-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b1042-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1042-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b1042-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1042-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b1042-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1042-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b1042-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1042-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
