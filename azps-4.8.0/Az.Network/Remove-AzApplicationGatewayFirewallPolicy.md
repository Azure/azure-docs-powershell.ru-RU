---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079455"
---
# <span data-ttu-id="7b950-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7b950-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="7b950-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b950-102">SYNOPSIS</span></span>
<span data-ttu-id="7b950-103">Удаление политики брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7b950-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="7b950-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b950-104">SYNTAX</span></span>

### <span data-ttu-id="7b950-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b950-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b950-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7b950-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b950-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b950-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b950-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b950-108">DESCRIPTION</span></span>
<span data-ttu-id="7b950-109">Командлет **Remove-AzApplicationGatewayFirewallPolicy** удаляет политику брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7b950-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="7b950-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b950-110">EXAMPLES</span></span>

### <span data-ttu-id="7b950-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b950-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7b950-112">Эта команда удаляет политику брандмауэра шлюза приложений с именем ApplicationGatewayFirewallPolicy01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7b950-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7b950-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b950-113">PARAMETERS</span></span>

### <span data-ttu-id="7b950-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b950-114">-AsJob</span></span>
<span data-ttu-id="7b950-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7b950-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b950-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b950-116">-DefaultProfile</span></span>
<span data-ttu-id="7b950-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b950-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b950-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7b950-118">-Force</span></span>
<span data-ttu-id="7b950-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7b950-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7b950-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b950-120">-InputObject</span></span>
<span data-ttu-id="7b950-121">Объект политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7b950-121">The firewall policy object</span></span>

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

### <span data-ttu-id="7b950-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b950-122">-Name</span></span>
<span data-ttu-id="7b950-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="7b950-123">The resource name.</span></span>

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

### <span data-ttu-id="7b950-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b950-124">-PassThru</span></span>
<span data-ttu-id="7b950-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7b950-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7b950-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7b950-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7b950-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b950-127">-ResourceGroupName</span></span>
<span data-ttu-id="7b950-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b950-128">The resource group name.</span></span>

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

### <span data-ttu-id="7b950-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b950-129">-ResourceId</span></span>
<span data-ttu-id="7b950-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7b950-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7b950-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b950-131">-Confirm</span></span>
<span data-ttu-id="7b950-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b950-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b950-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b950-133">-WhatIf</span></span>
<span data-ttu-id="7b950-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b950-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b950-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b950-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b950-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b950-136">CommonParameters</span></span>
<span data-ttu-id="7b950-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b950-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b950-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b950-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b950-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b950-139">INPUTS</span></span>

### <span data-ttu-id="7b950-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7b950-140">System.String</span></span>

## <span data-ttu-id="7b950-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b950-141">OUTPUTS</span></span>

### <span data-ttu-id="7b950-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b950-142">System.Boolean</span></span>

## <span data-ttu-id="7b950-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b950-143">NOTES</span></span>

## <span data-ttu-id="7b950-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b950-144">RELATED LINKS</span></span>