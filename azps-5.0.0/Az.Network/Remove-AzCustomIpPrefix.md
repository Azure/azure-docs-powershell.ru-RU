---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248244"
---
# <span data-ttu-id="2056b-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2056b-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="2056b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2056b-102">SYNOPSIS</span></span>
<span data-ttu-id="2056b-103">Удаление CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2056b-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="2056b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2056b-104">SYNTAX</span></span>

### <span data-ttu-id="2056b-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2056b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2056b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2056b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2056b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2056b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2056b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2056b-108">DESCRIPTION</span></span>
<span data-ttu-id="2056b-109">Командлет **Remove-AzCustomIpPrefix** удаляет CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2056b-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="2056b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2056b-110">EXAMPLES</span></span>

### <span data-ttu-id="2056b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2056b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="2056b-112">Удаление CustomIpPrefix с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="2056b-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="2056b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2056b-113">PARAMETERS</span></span>

### <span data-ttu-id="2056b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2056b-114">-AsJob</span></span>
<span data-ttu-id="2056b-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2056b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2056b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2056b-116">-DefaultProfile</span></span>
<span data-ttu-id="2056b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2056b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2056b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2056b-118">-Force</span></span>
<span data-ttu-id="2056b-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2056b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2056b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2056b-120">-InputObject</span></span>
<span data-ttu-id="2056b-121">Объект customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2056b-121">A customIpPrefix object.</span></span>

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

### <span data-ttu-id="2056b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2056b-122">-Name</span></span>
<span data-ttu-id="2056b-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2056b-123">The resource name.</span></span>

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

### <span data-ttu-id="2056b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2056b-124">-PassThru</span></span>
<span data-ttu-id="2056b-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2056b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2056b-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2056b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2056b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2056b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2056b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2056b-128">The resource group name.</span></span>

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

### <span data-ttu-id="2056b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2056b-129">-ResourceId</span></span>
<span data-ttu-id="2056b-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2056b-130">The resource id.</span></span>

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

### <span data-ttu-id="2056b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2056b-131">-Confirm</span></span>
<span data-ttu-id="2056b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2056b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2056b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2056b-133">-WhatIf</span></span>
<span data-ttu-id="2056b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2056b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2056b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2056b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2056b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2056b-136">CommonParameters</span></span>
<span data-ttu-id="2056b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2056b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2056b-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2056b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2056b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2056b-139">INPUTS</span></span>

### <span data-ttu-id="2056b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2056b-140">System.String</span></span>

### <span data-ttu-id="2056b-141">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2056b-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="2056b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2056b-142">OUTPUTS</span></span>

### <span data-ttu-id="2056b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2056b-143">System.Boolean</span></span>

## <span data-ttu-id="2056b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="2056b-144">NOTES</span></span>

## <span data-ttu-id="2056b-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2056b-145">RELATED LINKS</span></span>

[<span data-ttu-id="2056b-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2056b-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="2056b-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2056b-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="2056b-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2056b-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)