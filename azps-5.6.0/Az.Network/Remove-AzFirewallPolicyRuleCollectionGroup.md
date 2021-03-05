---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 50dd0f1b4f224b343d827ed3d07457d86352e96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993754"
---
# <span data-ttu-id="d6208-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d6208-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d6208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6208-102">SYNOPSIS</span></span>
<span data-ttu-id="d6208-103">Удаление группы правил брандмауэра Azure в политике брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d6208-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="d6208-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6208-104">SYNTAX</span></span>

### <span data-ttu-id="d6208-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6208-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6208-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6208-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6208-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6208-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6208-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6208-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6208-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6208-109">DESCRIPTION</span></span>
<span data-ttu-id="d6208-110">С **помощью cmdlet Remove-AzFirewallPolicyRuleCollectionGroup** группа коллекции правил удаляется из политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d6208-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d6208-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6208-111">EXAMPLES</span></span>

### <span data-ttu-id="d6208-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6208-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="d6208-113">В этом примере удаляется группа colelction правил брандмауэра с именем testRcGroup в объекте политики брандмауэра $fp</span><span class="sxs-lookup"><span data-stu-id="d6208-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="d6208-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d6208-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="d6208-115">В этом примере удаляется группа colelction правил брандмауэра с именем testRcGroup в брандмауэре fpName, frpm the resourcegroup names "testRg"</span><span class="sxs-lookup"><span data-stu-id="d6208-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="d6208-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6208-116">PARAMETERS</span></span>

### <span data-ttu-id="d6208-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6208-117">-AsJob</span></span>
<span data-ttu-id="d6208-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d6208-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6208-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6208-119">-DefaultProfile</span></span>
<span data-ttu-id="d6208-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6208-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="d6208-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="d6208-122">Имя политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="d6208-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d6208-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="d6208-124">Политика брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d6208-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d6208-125">-Force</span></span>
<span data-ttu-id="d6208-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d6208-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d6208-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6208-127">-InputObject</span></span>
<span data-ttu-id="d6208-128">Объект группы «Правила политики брандмауэра»</span><span class="sxs-lookup"><span data-stu-id="d6208-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d6208-129">-Name</span></span>
<span data-ttu-id="d6208-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d6208-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6208-131">-PassThru</span></span>
<span data-ttu-id="d6208-132">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d6208-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6208-133">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d6208-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6208-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6208-134">-ResourceGroupName</span></span>
<span data-ttu-id="d6208-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6208-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6208-136">-ResourceId</span></span>
<span data-ttu-id="d6208-137">ИД ресурса группы коллекции правил</span><span class="sxs-lookup"><span data-stu-id="d6208-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6208-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6208-138">-Confirm</span></span>
<span data-ttu-id="d6208-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d6208-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6208-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6208-140">-WhatIf</span></span>
<span data-ttu-id="d6208-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6208-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6208-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d6208-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6208-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6208-143">CommonParameters</span></span>
<span data-ttu-id="d6208-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6208-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6208-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6208-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6208-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6208-146">INPUTS</span></span>

### <span data-ttu-id="d6208-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d6208-147">System.String</span></span>

### <span data-ttu-id="d6208-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d6208-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="d6208-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="d6208-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="d6208-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6208-150">OUTPUTS</span></span>

### <span data-ttu-id="d6208-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6208-151">System.Boolean</span></span>

## <span data-ttu-id="d6208-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6208-152">NOTES</span></span>

## <span data-ttu-id="d6208-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6208-153">RELATED LINKS</span></span>
