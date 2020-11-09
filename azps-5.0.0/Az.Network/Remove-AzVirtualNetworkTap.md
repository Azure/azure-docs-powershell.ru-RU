---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248822"
---
# <span data-ttu-id="39485-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39485-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="39485-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39485-102">SYNOPSIS</span></span>
<span data-ttu-id="39485-103">Удаляет виртуальную сеть TAP.</span><span class="sxs-lookup"><span data-stu-id="39485-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="39485-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39485-104">SYNTAX</span></span>

### <span data-ttu-id="39485-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39485-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39485-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39485-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39485-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39485-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39485-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39485-108">DESCRIPTION</span></span>
<span data-ttu-id="39485-109">Командлет **Remove-AzVirtualNetworkTap** удаляет виртуальную сеть Azure TAP.</span><span class="sxs-lookup"><span data-stu-id="39485-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="39485-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39485-110">EXAMPLES</span></span>

### <span data-ttu-id="39485-111">Пример 1: Удаление виртуального сетевого касания</span><span class="sxs-lookup"><span data-stu-id="39485-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="39485-112">Эта команда удаляет VirtualNetworkTap1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="39485-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="39485-113">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="39485-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="39485-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39485-114">PARAMETERS</span></span>

### <span data-ttu-id="39485-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39485-115">-AsJob</span></span>
<span data-ttu-id="39485-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="39485-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39485-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39485-117">-DefaultProfile</span></span>
<span data-ttu-id="39485-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39485-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39485-119">-Force</span><span class="sxs-lookup"><span data-stu-id="39485-119">-Force</span></span>
<span data-ttu-id="39485-120">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="39485-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="39485-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39485-121">-InputObject</span></span>
<span data-ttu-id="39485-122">Ссылка на ресурс VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39485-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="39485-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39485-123">-Name</span></span>
<span data-ttu-id="39485-124">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="39485-124">The name of the tap.</span></span>

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

### <span data-ttu-id="39485-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39485-125">-PassThru</span></span>
<span data-ttu-id="39485-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="39485-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39485-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="39485-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39485-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39485-128">-ResourceGroupName</span></span>
<span data-ttu-id="39485-129">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="39485-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="39485-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39485-130">-ResourceId</span></span>
<span data-ttu-id="39485-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="39485-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="39485-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39485-132">-Confirm</span></span>
<span data-ttu-id="39485-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39485-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39485-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39485-134">-WhatIf</span></span>
<span data-ttu-id="39485-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39485-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39485-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39485-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39485-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39485-137">CommonParameters</span></span>
<span data-ttu-id="39485-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39485-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39485-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39485-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39485-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39485-140">INPUTS</span></span>

### <span data-ttu-id="39485-141">System. String</span><span class="sxs-lookup"><span data-stu-id="39485-141">System.String</span></span>

### <span data-ttu-id="39485-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39485-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="39485-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39485-143">OUTPUTS</span></span>

### <span data-ttu-id="39485-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39485-144">System.Boolean</span></span>

## <span data-ttu-id="39485-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="39485-145">NOTES</span></span>

## <span data-ttu-id="39485-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39485-146">RELATED LINKS</span></span>

[<span data-ttu-id="39485-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39485-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="39485-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39485-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="39485-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39485-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)