---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246085"
---
# <span data-ttu-id="c4245-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c4245-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="c4245-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4245-102">SYNOPSIS</span></span>
<span data-ttu-id="c4245-103">Удаление IpAllocation Azure.</span><span class="sxs-lookup"><span data-stu-id="c4245-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="c4245-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4245-104">SYNTAX</span></span>

### <span data-ttu-id="c4245-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4245-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4245-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4245-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4245-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4245-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4245-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4245-108">DESCRIPTION</span></span>
<span data-ttu-id="c4245-109">Командлет **Remove-AzIpAllocation** удаляет Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c4245-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="c4245-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4245-110">EXAMPLES</span></span>

### <span data-ttu-id="c4245-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4245-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="c4245-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4245-112">PARAMETERS</span></span>

### <span data-ttu-id="c4245-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4245-113">-AsJob</span></span>
<span data-ttu-id="c4245-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c4245-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4245-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4245-115">-DefaultProfile</span></span>
<span data-ttu-id="c4245-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4245-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4245-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c4245-117">-Force</span></span>
<span data-ttu-id="c4245-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c4245-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c4245-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4245-119">-InputObject</span></span>
<span data-ttu-id="c4245-120">{{Fill InputObject описание}}</span><span class="sxs-lookup"><span data-stu-id="c4245-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4245-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4245-121">-Name</span></span>
<span data-ttu-id="c4245-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c4245-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4245-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4245-123">-PassThru</span></span>
<span data-ttu-id="c4245-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c4245-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4245-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c4245-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4245-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4245-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4245-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4245-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4245-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4245-128">-ResourceId</span></span>
<span data-ttu-id="c4245-129">Идентификатор ресурса IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="c4245-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="c4245-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4245-130">-Confirm</span></span>
<span data-ttu-id="c4245-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4245-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4245-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4245-132">-WhatIf</span></span>
<span data-ttu-id="c4245-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4245-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4245-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4245-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4245-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4245-135">CommonParameters</span></span>
<span data-ttu-id="c4245-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4245-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4245-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4245-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4245-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4245-138">INPUTS</span></span>

### <span data-ttu-id="c4245-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4245-139">System.String</span></span>

## <span data-ttu-id="c4245-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4245-140">OUTPUTS</span></span>

### <span data-ttu-id="c4245-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4245-141">System.Boolean</span></span>

## <span data-ttu-id="c4245-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4245-142">NOTES</span></span>

## <span data-ttu-id="c4245-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4245-143">RELATED LINKS</span></span>
