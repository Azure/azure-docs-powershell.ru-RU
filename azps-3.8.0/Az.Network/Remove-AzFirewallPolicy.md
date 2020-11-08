---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074046"
---
# <span data-ttu-id="f7ef4-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7ef4-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="f7ef4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ef4-103">Удаление политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="f7ef4-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="f7ef4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7ef4-104">SYNTAX</span></span>

### <span data-ttu-id="f7ef4-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7ef4-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7ef4-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7ef4-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7ef4-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7ef4-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7ef4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="f7ef4-109">Командлет **Remove-AzFirewallPolicy** удаляет политику брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f7ef4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7ef4-110">EXAMPLES</span></span>

### <span data-ttu-id="f7ef4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7ef4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="f7ef4-112">В этом примере удаляется политика брандмауэра с именем "firewallpolicy" в группе "resourcegroup" TestRg</span><span class="sxs-lookup"><span data-stu-id="f7ef4-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="f7ef4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f7ef4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="f7ef4-114">В этом примере удаляется политика брандмауэра по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="f7ef4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f7ef4-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="f7ef4-116">В этом примере удаляется политика брандмауэра $fp</span><span class="sxs-lookup"><span data-stu-id="f7ef4-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="f7ef4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7ef4-117">PARAMETERS</span></span>

### <span data-ttu-id="f7ef4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7ef4-118">-AsJob</span></span>
<span data-ttu-id="f7ef4-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f7ef4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7ef4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ef4-120">-DefaultProfile</span></span>
<span data-ttu-id="f7ef4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ef4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f7ef4-122">-Force</span></span>
<span data-ttu-id="f7ef4-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f7ef4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7ef4-124">-InputObject</span></span>
<span data-ttu-id="f7ef4-125">Политика AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f7ef4-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ef4-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7ef4-126">-Name</span></span>
<span data-ttu-id="f7ef4-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ef4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7ef4-128">-PassThru</span></span>
<span data-ttu-id="f7ef4-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f7ef4-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7ef4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ef4-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7ef4-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ef4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7ef4-133">-ResourceId</span></span>
<span data-ttu-id="f7ef4-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ef4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7ef4-135">-Confirm</span></span>
<span data-ttu-id="f7ef4-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ef4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ef4-137">-WhatIf</span></span>
<span data-ttu-id="f7ef4-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7ef4-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ef4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ef4-140">CommonParameters</span></span>
<span data-ttu-id="f7ef4-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7ef4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ef4-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7ef4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ef4-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7ef4-143">INPUTS</span></span>

### <span data-ttu-id="f7ef4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f7ef4-144">System.String</span></span>

### <span data-ttu-id="f7ef4-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7ef4-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="f7ef4-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7ef4-146">OUTPUTS</span></span>

### <span data-ttu-id="f7ef4-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7ef4-147">System.Boolean</span></span>

## <span data-ttu-id="f7ef4-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7ef4-148">NOTES</span></span>

## <span data-ttu-id="f7ef4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7ef4-149">RELATED LINKS</span></span>
