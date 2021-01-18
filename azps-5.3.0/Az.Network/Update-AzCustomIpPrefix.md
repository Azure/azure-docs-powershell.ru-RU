---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505480"
---
# <span data-ttu-id="53d53-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="53d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53d53-102">SYNOPSIS</span></span>
<span data-ttu-id="53d53-103">Обновление customIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="53d53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53d53-104">SYNTAX</span></span>

### <span data-ttu-id="53d53-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53d53-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53d53-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53d53-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53d53-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53d53-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53d53-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53d53-108">DESCRIPTION</span></span>
<span data-ttu-id="53d53-109">Командлет **Update-AzCustomIpPrefix** позволяет пользователю взимание комиссионных или списание customIpPrefix или изменение тегов ресурса.</span><span class="sxs-lookup"><span data-stu-id="53d53-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="53d53-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53d53-110">EXAMPLES</span></span>

### <span data-ttu-id="53d53-111">Пример 1. Комиссионные для CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="53d53-112">С этой команды начинается процесс ввода в эксплуатацию customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="53d53-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="53d53-113">Пример 2. Списание customIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="53d53-114">С этой команды начинается процесс декомиссии customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="53d53-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="53d53-115">Пример 3. Обновление тегов для customIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="53d53-116">При этом теги для customIpPrefix обновятся.</span><span class="sxs-lookup"><span data-stu-id="53d53-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="53d53-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53d53-117">PARAMETERS</span></span>

### <span data-ttu-id="53d53-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53d53-118">-AsJob</span></span>
<span data-ttu-id="53d53-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="53d53-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53d53-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="53d53-120">-Commission</span></span>
<span data-ttu-id="53d53-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="53d53-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53d53-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="53d53-122">-Decomission</span></span>
<span data-ttu-id="53d53-123">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="53d53-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53d53-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d53-124">-DefaultProfile</span></span>
<span data-ttu-id="53d53-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53d53-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53d53-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53d53-126">-InputObject</span></span>
<span data-ttu-id="53d53-127">Настраиваемый Префикс для настройки.</span><span class="sxs-lookup"><span data-stu-id="53d53-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="53d53-128">-Name</span><span class="sxs-lookup"><span data-stu-id="53d53-128">-Name</span></span>
<span data-ttu-id="53d53-129">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="53d53-129">The resource name.</span></span>

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

### <span data-ttu-id="53d53-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53d53-130">-ResourceGroupName</span></span>
<span data-ttu-id="53d53-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53d53-131">The resource group name.</span></span>

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

### <span data-ttu-id="53d53-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53d53-132">-ResourceId</span></span>
<span data-ttu-id="53d53-133">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="53d53-133">The resource Id.</span></span>

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

### <span data-ttu-id="53d53-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="53d53-134">-Tag</span></span>
<span data-ttu-id="53d53-135">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="53d53-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="53d53-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53d53-136">-Confirm</span></span>
<span data-ttu-id="53d53-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="53d53-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53d53-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53d53-138">-WhatIf</span></span>
<span data-ttu-id="53d53-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53d53-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53d53-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53d53-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53d53-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d53-141">CommonParameters</span></span>
<span data-ttu-id="53d53-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d53-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d53-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53d53-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d53-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53d53-144">INPUTS</span></span>

### <span data-ttu-id="53d53-145">System.String</span><span class="sxs-lookup"><span data-stu-id="53d53-145">System.String</span></span>

### <span data-ttu-id="53d53-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="53d53-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53d53-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53d53-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53d53-148">OUTPUTS</span></span>

### <span data-ttu-id="53d53-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="53d53-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53d53-150">NOTES</span></span>

## <span data-ttu-id="53d53-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53d53-151">RELATED LINKS</span></span>

[<span data-ttu-id="53d53-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="53d53-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="53d53-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53d53-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)