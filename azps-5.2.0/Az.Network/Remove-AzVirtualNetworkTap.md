---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407335"
---
# <span data-ttu-id="5d8aa-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5d8aa-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="5d8aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8aa-103">Удаляет виртуальное сетевое касание.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="5d8aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d8aa-104">SYNTAX</span></span>

### <span data-ttu-id="5d8aa-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d8aa-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8aa-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d8aa-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8aa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d8aa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d8aa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8aa-108">DESCRIPTION</span></span>
<span data-ttu-id="5d8aa-109">Командлет **Remove-AzVirtualNetworkTap** удаляет виртуальный сетевой касание Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="5d8aa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d8aa-110">EXAMPLES</span></span>

### <span data-ttu-id="5d8aa-111">Пример 1. Удаление виртуального сетевого касания</span><span class="sxs-lookup"><span data-stu-id="5d8aa-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="5d8aa-112">Эта команда удаляет VirtualNetworkTap1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5d8aa-113">Так как *параметр Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="5d8aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d8aa-114">PARAMETERS</span></span>

### <span data-ttu-id="5d8aa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d8aa-115">-AsJob</span></span>
<span data-ttu-id="5d8aa-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5d8aa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d8aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8aa-117">-DefaultProfile</span></span>
<span data-ttu-id="5d8aa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d8aa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5d8aa-119">-Force</span></span>
<span data-ttu-id="5d8aa-120">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="5d8aa-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="5d8aa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d8aa-121">-InputObject</span></span>
<span data-ttu-id="5d8aa-122">Ссылка на ресурс VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5d8aa-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8aa-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5d8aa-123">-Name</span></span>
<span data-ttu-id="5d8aa-124">Имя касания.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-124">The name of the tap.</span></span>

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

### <span data-ttu-id="5d8aa-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d8aa-125">-PassThru</span></span>
<span data-ttu-id="5d8aa-126">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5d8aa-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d8aa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d8aa-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d8aa-129">Имя группы ресурсов виртуального сетевого касания.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="5d8aa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d8aa-130">-ResourceId</span></span>
<span data-ttu-id="5d8aa-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="5d8aa-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8aa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d8aa-132">-Confirm</span></span>
<span data-ttu-id="5d8aa-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8aa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8aa-134">-WhatIf</span></span>
<span data-ttu-id="5d8aa-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d8aa-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8aa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8aa-137">CommonParameters</span></span>
<span data-ttu-id="5d8aa-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8aa-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d8aa-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8aa-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d8aa-140">INPUTS</span></span>

### <span data-ttu-id="5d8aa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5d8aa-141">System.String</span></span>

### <span data-ttu-id="5d8aa-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5d8aa-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="5d8aa-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d8aa-143">OUTPUTS</span></span>

### <span data-ttu-id="5d8aa-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d8aa-144">System.Boolean</span></span>

## <span data-ttu-id="5d8aa-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d8aa-145">NOTES</span></span>

## <span data-ttu-id="5d8aa-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d8aa-146">RELATED LINKS</span></span>

[<span data-ttu-id="5d8aa-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5d8aa-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="5d8aa-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5d8aa-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="5d8aa-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5d8aa-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
