---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244348"
---
# <span data-ttu-id="d36c3-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d36c3-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="d36c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d36c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d36c3-103">Удаление CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d36c3-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="d36c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d36c3-104">SYNTAX</span></span>

### <span data-ttu-id="d36c3-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d36c3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d36c3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d36c3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d36c3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d36c3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d36c3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d36c3-108">DESCRIPTION</span></span>
<span data-ttu-id="d36c3-109">Командлет **Remove-AzCustomIpPrefix** удаляет CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d36c3-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="d36c3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d36c3-110">EXAMPLES</span></span>

### <span data-ttu-id="d36c3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d36c3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="d36c3-112">Удаление CustomIpPrefix с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="d36c3-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="d36c3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d36c3-113">PARAMETERS</span></span>

### <span data-ttu-id="d36c3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d36c3-114">-AsJob</span></span>
<span data-ttu-id="d36c3-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d36c3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d36c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36c3-116">-DefaultProfile</span></span>
<span data-ttu-id="d36c3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d36c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d36c3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d36c3-118">-Force</span></span>
<span data-ttu-id="d36c3-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d36c3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d36c3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d36c3-120">-InputObject</span></span>
<span data-ttu-id="d36c3-121">Объект customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d36c3-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d36c3-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d36c3-122">-Name</span></span>
<span data-ttu-id="d36c3-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d36c3-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36c3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d36c3-124">-PassThru</span></span>
<span data-ttu-id="d36c3-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d36c3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d36c3-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d36c3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d36c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d36c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="d36c3-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d36c3-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36c3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d36c3-129">-ResourceId</span></span>
<span data-ttu-id="d36c3-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d36c3-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36c3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d36c3-131">-Confirm</span></span>
<span data-ttu-id="d36c3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d36c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d36c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d36c3-133">-WhatIf</span></span>
<span data-ttu-id="d36c3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d36c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d36c3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d36c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d36c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36c3-136">CommonParameters</span></span>
<span data-ttu-id="d36c3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d36c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36c3-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d36c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36c3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d36c3-139">INPUTS</span></span>

### <span data-ttu-id="d36c3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d36c3-140">System.String</span></span>

### <span data-ttu-id="d36c3-141">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d36c3-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="d36c3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d36c3-142">OUTPUTS</span></span>

### <span data-ttu-id="d36c3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d36c3-143">System.Boolean</span></span>

## <span data-ttu-id="d36c3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d36c3-144">NOTES</span></span>

## <span data-ttu-id="d36c3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d36c3-145">RELATED LINKS</span></span>

[<span data-ttu-id="d36c3-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d36c3-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="d36c3-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d36c3-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="d36c3-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d36c3-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)