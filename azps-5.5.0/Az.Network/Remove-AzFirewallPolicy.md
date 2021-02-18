---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240685"
---
# <span data-ttu-id="d8fe8-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d8fe8-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="d8fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="d8fe8-103">Удаление политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d8fe8-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="d8fe8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8fe8-104">SYNTAX</span></span>

### <span data-ttu-id="d8fe8-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8fe8-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8fe8-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8fe8-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8fe8-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8fe8-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8fe8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="d8fe8-109">С **помощью cmdlet Remove-AzFirewallPolicy** политика брандмауэра Azure удаляется.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d8fe8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8fe8-110">EXAMPLES</span></span>

### <span data-ttu-id="d8fe8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8fe8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="d8fe8-112">В этом примере удаляется политика брандмауэра firewallpolicy из группы ресурсов TestRg.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="d8fe8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8fe8-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="d8fe8-114">В этом примере политика брандмауэра удаляется с помощью ИД.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="d8fe8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d8fe8-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="d8fe8-116">В этом примере политика брандмауэра удаляется $fp</span><span class="sxs-lookup"><span data-stu-id="d8fe8-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="d8fe8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8fe8-117">PARAMETERS</span></span>

### <span data-ttu-id="d8fe8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8fe8-118">-AsJob</span></span>
<span data-ttu-id="d8fe8-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8fe8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8fe8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8fe8-120">-DefaultProfile</span></span>
<span data-ttu-id="d8fe8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8fe8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d8fe8-122">-Force</span></span>
<span data-ttu-id="d8fe8-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d8fe8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8fe8-124">-InputObject</span></span>
<span data-ttu-id="d8fe8-125">Политика AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d8fe8-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="d8fe8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d8fe8-126">-Name</span></span>
<span data-ttu-id="d8fe8-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-127">The resource name.</span></span>

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

### <span data-ttu-id="d8fe8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8fe8-128">-PassThru</span></span>
<span data-ttu-id="d8fe8-129">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d8fe8-130">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8fe8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8fe8-131">-ResourceGroupName</span></span>
<span data-ttu-id="d8fe8-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-132">The resource group name.</span></span>

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

### <span data-ttu-id="d8fe8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8fe8-133">-ResourceId</span></span>
<span data-ttu-id="d8fe8-134">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-134">The resource Id.</span></span>

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

### <span data-ttu-id="d8fe8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8fe8-135">-Confirm</span></span>
<span data-ttu-id="d8fe8-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8fe8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8fe8-137">-WhatIf</span></span>
<span data-ttu-id="d8fe8-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8fe8-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8fe8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8fe8-140">CommonParameters</span></span>
<span data-ttu-id="d8fe8-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8fe8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8fe8-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8fe8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8fe8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8fe8-143">INPUTS</span></span>

### <span data-ttu-id="d8fe8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d8fe8-144">System.String</span></span>

### <span data-ttu-id="d8fe8-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d8fe8-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="d8fe8-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8fe8-146">OUTPUTS</span></span>

### <span data-ttu-id="d8fe8-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8fe8-147">System.Boolean</span></span>

## <span data-ttu-id="d8fe8-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8fe8-148">NOTES</span></span>

## <span data-ttu-id="d8fe8-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8fe8-149">RELATED LINKS</span></span>
