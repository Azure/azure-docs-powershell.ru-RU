---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 82fdec48f2e021e33490f84a05a064fb007ac8d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560267"
---
# <span data-ttu-id="f6a72-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6a72-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="f6a72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6a72-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a72-103">Создание группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="f6a72-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6a72-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6a72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a72-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a72-106">Командлет **New-AzureRmApplicationSecurityGroup** создает группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="f6a72-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="f6a72-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6a72-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a72-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6a72-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="f6a72-109">В этом примере создается группа безопасности приложения без ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="f6a72-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="f6a72-110">После создания IP-конфигурации в сетевом интерфейсе можно включить в группу.</span><span class="sxs-lookup"><span data-stu-id="f6a72-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="f6a72-111">Правила безопасности могут также ссылаться на группу в качестве источников или назначений.</span><span class="sxs-lookup"><span data-stu-id="f6a72-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="f6a72-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6a72-112">PARAMETERS</span></span>

### <span data-ttu-id="f6a72-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6a72-113">-AsJob</span></span>
<span data-ttu-id="f6a72-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f6a72-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a72-115">-DefaultProfile</span></span>
<span data-ttu-id="f6a72-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a72-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f6a72-117">-Force</span></span>
<span data-ttu-id="f6a72-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс.</span><span class="sxs-lookup"><span data-stu-id="f6a72-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f6a72-119">-Location</span></span>
<span data-ttu-id="f6a72-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="f6a72-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6a72-121">-Name</span></span>
<span data-ttu-id="f6a72-122">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="f6a72-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a72-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6a72-124">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="f6a72-124">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="f6a72-125">-Tag</span></span>
<span data-ttu-id="f6a72-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6a72-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6a72-127">-Confirm</span></span>
<span data-ttu-id="f6a72-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6a72-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a72-129">-WhatIf</span></span>
<span data-ttu-id="f6a72-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6a72-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a72-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6a72-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a72-132">CommonParameters</span></span>
<span data-ttu-id="f6a72-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6a72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a72-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a72-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a72-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6a72-135">INPUTS</span></span>

### <span data-ttu-id="f6a72-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f6a72-136">System.String</span></span>
<span data-ttu-id="f6a72-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6a72-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6a72-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a72-138">OUTPUTS</span></span>

### <span data-ttu-id="f6a72-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6a72-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="f6a72-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6a72-140">NOTES</span></span>

## <span data-ttu-id="f6a72-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6a72-141">RELATED LINKS</span></span>

[<span data-ttu-id="f6a72-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6a72-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="f6a72-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6a72-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="f6a72-144">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6a72-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f6a72-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6a72-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f6a72-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6a72-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f6a72-147">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f6a72-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f6a72-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f6a72-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f6a72-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f6a72-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
