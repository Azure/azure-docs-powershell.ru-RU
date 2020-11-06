---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562803"
---
# <span data-ttu-id="5e59a-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5e59a-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="5e59a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e59a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e59a-103">Удаляет виртуальную сеть TAP.</span><span class="sxs-lookup"><span data-stu-id="5e59a-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e59a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e59a-104">SYNTAX</span></span>

### <span data-ttu-id="5e59a-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e59a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e59a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e59a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e59a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e59a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e59a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e59a-108">DESCRIPTION</span></span>
<span data-ttu-id="5e59a-109">Командлет **Remove-AzureRmVirtualNetworkTap** удаляет виртуальную сеть Azure TAP.</span><span class="sxs-lookup"><span data-stu-id="5e59a-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="5e59a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e59a-110">EXAMPLES</span></span>

### <span data-ttu-id="5e59a-111">Пример 1: удаление virtuak сети нажмите</span><span class="sxs-lookup"><span data-stu-id="5e59a-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="5e59a-112">Эта команда удаляет VirtualNetworkTap1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="5e59a-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5e59a-113">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="5e59a-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="5e59a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e59a-114">PARAMETERS</span></span>

### <span data-ttu-id="5e59a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e59a-115">-AsJob</span></span>
<span data-ttu-id="5e59a-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5e59a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e59a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e59a-117">-DefaultProfile</span></span>
<span data-ttu-id="5e59a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e59a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e59a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5e59a-119">-Force</span></span>
<span data-ttu-id="5e59a-120">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="5e59a-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="5e59a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e59a-121">-InputObject</span></span>
<span data-ttu-id="5e59a-122">Ссылка на ресурс VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5e59a-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="5e59a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e59a-123">-Name</span></span>
<span data-ttu-id="5e59a-124">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="5e59a-124">The name of the tap.</span></span>

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

### <span data-ttu-id="5e59a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e59a-125">-PassThru</span></span>
<span data-ttu-id="5e59a-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5e59a-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e59a-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5e59a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e59a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e59a-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e59a-129">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="5e59a-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="5e59a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e59a-130">-ResourceId</span></span>
<span data-ttu-id="5e59a-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="5e59a-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="5e59a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e59a-132">-Confirm</span></span>
<span data-ttu-id="5e59a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e59a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e59a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e59a-134">-WhatIf</span></span>
<span data-ttu-id="5e59a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e59a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e59a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e59a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e59a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e59a-137">CommonParameters</span></span>
<span data-ttu-id="5e59a-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e59a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e59a-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e59a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e59a-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e59a-140">INPUTS</span></span>

### <span data-ttu-id="5e59a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5e59a-141">System.String</span></span>

## <span data-ttu-id="5e59a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e59a-142">OUTPUTS</span></span>

### <span data-ttu-id="5e59a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e59a-143">System.Boolean</span></span>

## <span data-ttu-id="5e59a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e59a-144">NOTES</span></span>

## <span data-ttu-id="5e59a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e59a-145">RELATED LINKS</span></span>
