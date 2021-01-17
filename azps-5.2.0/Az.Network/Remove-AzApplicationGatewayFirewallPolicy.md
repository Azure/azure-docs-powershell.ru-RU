---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401716"
---
# <span data-ttu-id="7592d-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7592d-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="7592d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7592d-102">SYNOPSIS</span></span>
<span data-ttu-id="7592d-103">Удаляет политику брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7592d-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="7592d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7592d-104">SYNTAX</span></span>

### <span data-ttu-id="7592d-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7592d-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7592d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7592d-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7592d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7592d-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7592d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7592d-108">DESCRIPTION</span></span>
<span data-ttu-id="7592d-109">С **помощью cmdlet Remove-AzApplicationGatewayFirewallPolicy** политика брандмауэра шлюза приложения удаляется.</span><span class="sxs-lookup"><span data-stu-id="7592d-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="7592d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7592d-110">EXAMPLES</span></span>

### <span data-ttu-id="7592d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7592d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7592d-112">Эта команда удаляет политику брандмауэра шлюза приложения ApplicationGatewayFirewallPolicy01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7592d-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7592d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7592d-113">PARAMETERS</span></span>

### <span data-ttu-id="7592d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7592d-114">-AsJob</span></span>
<span data-ttu-id="7592d-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7592d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7592d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7592d-116">-DefaultProfile</span></span>
<span data-ttu-id="7592d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7592d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7592d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7592d-118">-Force</span></span>
<span data-ttu-id="7592d-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7592d-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7592d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7592d-120">-InputObject</span></span>
<span data-ttu-id="7592d-121">Объект политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7592d-121">The firewall policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7592d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7592d-122">-Name</span></span>
<span data-ttu-id="7592d-123">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="7592d-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7592d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7592d-124">-PassThru</span></span>
<span data-ttu-id="7592d-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7592d-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7592d-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7592d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7592d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7592d-127">-ResourceGroupName</span></span>
<span data-ttu-id="7592d-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7592d-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7592d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7592d-129">-ResourceId</span></span>
<span data-ttu-id="7592d-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7592d-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7592d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7592d-131">-Confirm</span></span>
<span data-ttu-id="7592d-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7592d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7592d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7592d-133">-WhatIf</span></span>
<span data-ttu-id="7592d-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7592d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7592d-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7592d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7592d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7592d-136">CommonParameters</span></span>
<span data-ttu-id="7592d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7592d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7592d-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7592d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7592d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7592d-139">INPUTS</span></span>

### <span data-ttu-id="7592d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7592d-140">System.String</span></span>

## <span data-ttu-id="7592d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7592d-141">OUTPUTS</span></span>

### <span data-ttu-id="7592d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7592d-142">System.Boolean</span></span>

## <span data-ttu-id="7592d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7592d-143">NOTES</span></span>

## <span data-ttu-id="7592d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7592d-144">RELATED LINKS</span></span>
