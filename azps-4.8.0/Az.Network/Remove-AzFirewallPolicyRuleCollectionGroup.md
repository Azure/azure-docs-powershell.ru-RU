---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079441"
---
# <span data-ttu-id="0ff2a-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="0ff2a-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="0ff2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ff2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff2a-103">Удаление группы набора правил политики брандмауэра Azure в политике брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="0ff2a-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="0ff2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ff2a-104">SYNTAX</span></span>

### <span data-ttu-id="0ff2a-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ff2a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff2a-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ff2a-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ff2a-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ff2a-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ff2a-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ff2a-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff2a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-109">DESCRIPTION</span></span>
<span data-ttu-id="0ff2a-110">Командлет **Remove-AzFirewallPolicyRuleCollectionGroup** удаляет группу семейства правил из политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="0ff2a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-111">EXAMPLES</span></span>

### <span data-ttu-id="0ff2a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ff2a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="0ff2a-113">В этом примере удаляется группа "правила политики брандмауэра" colelction с именем "testRcGroup" в объекте политики брандмауэра $fp</span><span class="sxs-lookup"><span data-stu-id="0ff2a-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="0ff2a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0ff2a-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="0ff2a-115">В этом примере удаляется группа colelction правила политики межсетевого экрана с именем "testRcGroup" в брандмауэре с именем "fpName" frpm именами resourcegroup "testRg".</span><span class="sxs-lookup"><span data-stu-id="0ff2a-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="0ff2a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-116">PARAMETERS</span></span>

### <span data-ttu-id="0ff2a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ff2a-117">-AsJob</span></span>
<span data-ttu-id="0ff2a-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0ff2a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ff2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff2a-119">-DefaultProfile</span></span>
<span data-ttu-id="0ff2a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ff2a-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="0ff2a-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="0ff2a-122">Имя политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="0ff2a-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="0ff2a-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0ff2a-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="0ff2a-124">Политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="0ff2a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0ff2a-125">-Force</span></span>
<span data-ttu-id="0ff2a-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0ff2a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ff2a-127">-InputObject</span></span>
<span data-ttu-id="0ff2a-128">Объект группы набора правил политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="0ff2a-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="0ff2a-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ff2a-129">-Name</span></span>
<span data-ttu-id="0ff2a-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-130">The resource name.</span></span>

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

### <span data-ttu-id="0ff2a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ff2a-131">-PassThru</span></span>
<span data-ttu-id="0ff2a-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ff2a-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ff2a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff2a-134">-ResourceGroupName</span></span>
<span data-ttu-id="0ff2a-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-135">The resource group name.</span></span>

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

### <span data-ttu-id="0ff2a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ff2a-136">-ResourceId</span></span>
<span data-ttu-id="0ff2a-137">Идентификатор ресурса группы набора правил</span><span class="sxs-lookup"><span data-stu-id="0ff2a-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="0ff2a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ff2a-138">-Confirm</span></span>
<span data-ttu-id="0ff2a-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff2a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff2a-140">-WhatIf</span></span>
<span data-ttu-id="0ff2a-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff2a-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff2a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff2a-143">CommonParameters</span></span>
<span data-ttu-id="0ff2a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff2a-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ff2a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff2a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ff2a-146">INPUTS</span></span>

### <span data-ttu-id="0ff2a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff2a-147">System.String</span></span>

### <span data-ttu-id="0ff2a-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0ff2a-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="0ff2a-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="0ff2a-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="0ff2a-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-150">OUTPUTS</span></span>

### <span data-ttu-id="0ff2a-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ff2a-151">System.Boolean</span></span>

## <span data-ttu-id="0ff2a-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ff2a-152">NOTES</span></span>

## <span data-ttu-id="0ff2a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-153">RELATED LINKS</span></span>
