---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734044"
---
# <span data-ttu-id="1b882-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1b882-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="1b882-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b882-102">SYNOPSIS</span></span>
<span data-ttu-id="1b882-103">Создание группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="1b882-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b882-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b882-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b882-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b882-105">DESCRIPTION</span></span>
<span data-ttu-id="1b882-106">Командлет **New-AzureRmApplicationSecurityGroup** создает группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="1b882-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="1b882-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b882-107">EXAMPLES</span></span>

### <span data-ttu-id="1b882-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b882-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="1b882-109">В этом примере создается группа безопасности приложения без ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="1b882-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="1b882-110">После создания IP-конфигурации в сетевом интерфейсе можно включить в группу.</span><span class="sxs-lookup"><span data-stu-id="1b882-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="1b882-111">Правила безопасности могут также ссылаться на группу в качестве источников или назначений.</span><span class="sxs-lookup"><span data-stu-id="1b882-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="1b882-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b882-112">PARAMETERS</span></span>

### <span data-ttu-id="1b882-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b882-113">-DefaultProfile</span></span>
<span data-ttu-id="1b882-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b882-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b882-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1b882-115">-Force</span></span>
<span data-ttu-id="1b882-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс.</span><span class="sxs-lookup"><span data-stu-id="1b882-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="1b882-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1b882-117">-Location</span></span>
<span data-ttu-id="1b882-118">Расположение.</span><span class="sxs-lookup"><span data-stu-id="1b882-118">The location.</span></span>

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

### <span data-ttu-id="1b882-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b882-119">-Name</span></span>
<span data-ttu-id="1b882-120">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="1b882-120">The name of the application security group.</span></span>

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

### <span data-ttu-id="1b882-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b882-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b882-122">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="1b882-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="1b882-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="1b882-123">-Tag</span></span>
<span data-ttu-id="1b882-124">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b882-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1b882-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b882-125">-Confirm</span></span>
<span data-ttu-id="1b882-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b882-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b882-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b882-127">-WhatIf</span></span>
<span data-ttu-id="1b882-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b882-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b882-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b882-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b882-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b882-130">CommonParameters</span></span>
<span data-ttu-id="1b882-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b882-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b882-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b882-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b882-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b882-133">INPUTS</span></span>

### <span data-ttu-id="1b882-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1b882-134">System.String</span></span>
<span data-ttu-id="1b882-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b882-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b882-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b882-136">OUTPUTS</span></span>

### <span data-ttu-id="1b882-137">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1b882-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="1b882-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b882-138">NOTES</span></span>

## <span data-ttu-id="1b882-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b882-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b882-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1b882-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="1b882-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1b882-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="1b882-142">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b882-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1b882-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b882-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1b882-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b882-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1b882-145">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b882-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1b882-146">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b882-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1b882-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b882-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
