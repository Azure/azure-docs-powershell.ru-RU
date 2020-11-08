---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244046"
---
# <span data-ttu-id="99d46-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="99d46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99d46-102">SYNOPSIS</span></span>
<span data-ttu-id="99d46-103">Обновляет CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="99d46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99d46-104">SYNTAX</span></span>

### <span data-ttu-id="99d46-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99d46-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99d46-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99d46-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d46-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99d46-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d46-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99d46-108">DESCRIPTION</span></span>
<span data-ttu-id="99d46-109">Командлет **Update-AzCustomIpPrefix** позволяет пользователю выступающие или списать CustomIpPrefix, а также изменять теги ресурса.</span><span class="sxs-lookup"><span data-stu-id="99d46-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="99d46-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99d46-110">EXAMPLES</span></span>

### <span data-ttu-id="99d46-111">Пример 1: Комиссия CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="99d46-112">Приведенная выше команда запускает процесс комиссий для CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="99d46-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="99d46-113">Пример 2: списание CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="99d46-114">В приведенной выше команде начинается процесс отмены Комиссии для CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="99d46-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="99d46-115">Пример 3: обновление тегов для CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="99d46-116">В приведенной выше команде будут обновлены теги для CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="99d46-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="99d46-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99d46-117">PARAMETERS</span></span>

### <span data-ttu-id="99d46-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99d46-118">-AsJob</span></span>
<span data-ttu-id="99d46-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="99d46-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99d46-120">-Комиссия</span><span class="sxs-lookup"><span data-stu-id="99d46-120">-Commission</span></span>
<span data-ttu-id="99d46-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="99d46-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99d46-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="99d46-122">-Decomission</span></span>
<span data-ttu-id="99d46-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="99d46-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99d46-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d46-124">-DefaultProfile</span></span>
<span data-ttu-id="99d46-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99d46-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d46-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99d46-126">-InputObject</span></span>
<span data-ttu-id="99d46-127">Заданный CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="99d46-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="99d46-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99d46-128">-Name</span></span>
<span data-ttu-id="99d46-129">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="99d46-129">The resource name.</span></span>

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

### <span data-ttu-id="99d46-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d46-130">-ResourceGroupName</span></span>
<span data-ttu-id="99d46-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99d46-131">The resource group name.</span></span>

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

### <span data-ttu-id="99d46-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99d46-132">-ResourceId</span></span>
<span data-ttu-id="99d46-133">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="99d46-133">The resource Id.</span></span>

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

### <span data-ttu-id="99d46-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="99d46-134">-Tag</span></span>
<span data-ttu-id="99d46-135">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99d46-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="99d46-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99d46-136">-Confirm</span></span>
<span data-ttu-id="99d46-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99d46-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d46-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d46-138">-WhatIf</span></span>
<span data-ttu-id="99d46-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99d46-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d46-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99d46-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d46-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d46-141">CommonParameters</span></span>
<span data-ttu-id="99d46-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99d46-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d46-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99d46-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d46-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99d46-144">INPUTS</span></span>

### <span data-ttu-id="99d46-145">System. String</span><span class="sxs-lookup"><span data-stu-id="99d46-145">System.String</span></span>

### <span data-ttu-id="99d46-146">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="99d46-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99d46-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="99d46-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99d46-148">OUTPUTS</span></span>

### <span data-ttu-id="99d46-149">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="99d46-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="99d46-150">NOTES</span></span>

## <span data-ttu-id="99d46-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99d46-151">RELATED LINKS</span></span>

[<span data-ttu-id="99d46-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="99d46-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="99d46-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99d46-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)