---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 6813bf30da73f09f285151d6d309eb89b32acbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730412"
---
# <span data-ttu-id="fd988-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fd988-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="fd988-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd988-102">SYNOPSIS</span></span>
<span data-ttu-id="fd988-103">Создание политики брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="fd988-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="fd988-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd988-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd988-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd988-105">DESCRIPTION</span></span>
<span data-ttu-id="fd988-106">Командлет **New-AzApplicationGatewayFirewallPolicy** создает политику брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="fd988-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="fd988-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd988-107">EXAMPLES</span></span>

### <span data-ttu-id="fd988-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd988-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzureRmApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="fd988-109">Эта команда создает новую политику брандмауэра для шлюза приложений Azure с именем "wafResource1" в группе ресурсов "Rg1" в папке "westus" с пользовательскими правилами, определенными в переменной $customRule</span><span class="sxs-lookup"><span data-stu-id="fd988-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="fd988-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd988-110">PARAMETERS</span></span>

### <span data-ttu-id="fd988-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd988-111">-AsJob</span></span>
<span data-ttu-id="fd988-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fd988-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd988-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="fd988-113">-CustomRule</span></span>
<span data-ttu-id="fd988-114">Список CustomRules</span><span class="sxs-lookup"><span data-stu-id="fd988-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd988-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd988-115">-DefaultProfile</span></span>
<span data-ttu-id="fd988-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd988-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd988-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fd988-117">-Force</span></span>
<span data-ttu-id="fd988-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="fd988-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd988-119">-Location</span><span class="sxs-lookup"><span data-stu-id="fd988-119">-Location</span></span>
<span data-ttu-id="fd988-120">поиска.</span><span class="sxs-lookup"><span data-stu-id="fd988-120">location.</span></span>

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

### <span data-ttu-id="fd988-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd988-121">-Name</span></span>
<span data-ttu-id="fd988-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fd988-122">The resource name.</span></span>

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

### <span data-ttu-id="fd988-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd988-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd988-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd988-124">The resource group name.</span></span>

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

### <span data-ttu-id="fd988-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="fd988-125">-Tag</span></span>
<span data-ttu-id="fd988-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd988-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fd988-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd988-127">-Confirm</span></span>
<span data-ttu-id="fd988-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd988-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd988-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd988-129">-WhatIf</span></span>
<span data-ttu-id="fd988-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd988-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd988-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd988-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd988-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd988-132">CommonParameters</span></span>
<span data-ttu-id="fd988-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd988-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd988-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd988-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd988-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd988-135">INPUTS</span></span>

### <span data-ttu-id="fd988-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fd988-136">System.String</span></span>

### <span data-ttu-id="fd988-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="fd988-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="fd988-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd988-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd988-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd988-139">OUTPUTS</span></span>

### <span data-ttu-id="fd988-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fd988-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="fd988-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd988-141">NOTES</span></span>

## <span data-ttu-id="fd988-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd988-142">RELATED LINKS</span></span>
