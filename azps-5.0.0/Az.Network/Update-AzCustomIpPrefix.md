---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318497"
---
# <span data-ttu-id="e95d2-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="e95d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e95d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e95d2-103">Обновляет CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="e95d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e95d2-104">SYNTAX</span></span>

### <span data-ttu-id="e95d2-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95d2-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e95d2-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95d2-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95d2-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95d2-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95d2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e95d2-108">DESCRIPTION</span></span>
<span data-ttu-id="e95d2-109">Командлет **Update-AzCustomIpPrefix** позволяет пользователю выступающие или списать CustomIpPrefix, а также изменять теги ресурса.</span><span class="sxs-lookup"><span data-stu-id="e95d2-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="e95d2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e95d2-110">EXAMPLES</span></span>

### <span data-ttu-id="e95d2-111">Пример 1: Комиссия CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="e95d2-112">Приведенная выше команда запускает процесс комиссий для CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e95d2-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="e95d2-113">Пример 2: списание CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="e95d2-114">В приведенной выше команде начинается процесс отмены Комиссии для CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e95d2-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="e95d2-115">Пример 3: обновление тегов для CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="e95d2-116">В приведенной выше команде будут обновлены теги для CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e95d2-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="e95d2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e95d2-117">PARAMETERS</span></span>

### <span data-ttu-id="e95d2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e95d2-118">-AsJob</span></span>
<span data-ttu-id="e95d2-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e95d2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95d2-120">-Комиссия</span><span class="sxs-lookup"><span data-stu-id="e95d2-120">-Commission</span></span>
<span data-ttu-id="e95d2-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e95d2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95d2-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="e95d2-122">-Decomission</span></span>
<span data-ttu-id="e95d2-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e95d2-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95d2-124">-DefaultProfile</span></span>
<span data-ttu-id="e95d2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e95d2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95d2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e95d2-126">-InputObject</span></span>
<span data-ttu-id="e95d2-127">Заданный CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e95d2-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d2-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e95d2-128">-Name</span></span>
<span data-ttu-id="e95d2-129">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e95d2-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95d2-130">-ResourceGroupName</span></span>
<span data-ttu-id="e95d2-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e95d2-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e95d2-132">-ResourceId</span></span>
<span data-ttu-id="e95d2-133">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e95d2-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d2-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="e95d2-134">-Tag</span></span>
<span data-ttu-id="e95d2-135">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e95d2-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e95d2-136">-Confirm</span></span>
<span data-ttu-id="e95d2-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e95d2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95d2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95d2-138">-WhatIf</span></span>
<span data-ttu-id="e95d2-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e95d2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95d2-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e95d2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95d2-141">CommonParameters</span></span>
<span data-ttu-id="e95d2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e95d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95d2-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e95d2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95d2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e95d2-144">INPUTS</span></span>

### <span data-ttu-id="e95d2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e95d2-145">System.String</span></span>

### <span data-ttu-id="e95d2-146">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="e95d2-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e95d2-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e95d2-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e95d2-148">OUTPUTS</span></span>

### <span data-ttu-id="e95d2-149">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="e95d2-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="e95d2-150">NOTES</span></span>

## <span data-ttu-id="e95d2-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e95d2-151">RELATED LINKS</span></span>

[<span data-ttu-id="e95d2-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="e95d2-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="e95d2-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e95d2-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)