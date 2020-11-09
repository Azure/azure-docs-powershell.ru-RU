---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317894"
---
# <span data-ttu-id="f88d2-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="f88d2-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="f88d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f88d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f88d2-103">Удалите или удалите зарегистрированный префикс из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="f88d2-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="f88d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f88d2-104">SYNTAX</span></span>

### <span data-ttu-id="f88d2-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f88d2-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f88d2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f88d2-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f88d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f88d2-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f88d2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f88d2-108">DESCRIPTION</span></span>
<span data-ttu-id="f88d2-109">Позволяет удалить зарегистрированный префикс из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="f88d2-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="f88d2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f88d2-110">EXAMPLES</span></span>

### <span data-ttu-id="f88d2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f88d2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="f88d2-112">Удалите регистрационный префикс, заданный идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="f88d2-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="f88d2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f88d2-113">PARAMETERS</span></span>

### <span data-ttu-id="f88d2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-114">-AsJob</span></span>
<span data-ttu-id="f88d2-115">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f88d2-115">Run in the background.</span></span>

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

### <span data-ttu-id="f88d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88d2-116">-DefaultProfile</span></span>
<span data-ttu-id="f88d2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f88d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88d2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f88d2-118">-Force</span></span>
<span data-ttu-id="f88d2-119">Принудительно завершить операцию</span><span class="sxs-lookup"><span data-stu-id="f88d2-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="f88d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f88d2-120">-InputObject</span></span>
<span data-ttu-id="f88d2-121">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f88d2-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f88d2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f88d2-122">-Name</span></span>
<span data-ttu-id="f88d2-123">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="f88d2-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f88d2-124">-PassThru</span></span>
<span data-ttu-id="f88d2-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="f88d2-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f88d2-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="f88d2-126">-PeeringName</span></span>
<span data-ttu-id="f88d2-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f88d2-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88d2-128">-ResourceGroupName</span></span>
<span data-ttu-id="f88d2-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f88d2-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f88d2-130">-ResourceId</span></span>
<span data-ttu-id="f88d2-131">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="f88d2-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f88d2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f88d2-132">-Confirm</span></span>
<span data-ttu-id="f88d2-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f88d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f88d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f88d2-134">-WhatIf</span></span>
<span data-ttu-id="f88d2-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f88d2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f88d2-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f88d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f88d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88d2-137">CommonParameters</span></span>
<span data-ttu-id="f88d2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f88d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88d2-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f88d2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88d2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f88d2-140">INPUTS</span></span>

### <span data-ttu-id="f88d2-141">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="f88d2-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="f88d2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f88d2-142">System.String</span></span>

## <span data-ttu-id="f88d2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f88d2-143">OUTPUTS</span></span>

### <span data-ttu-id="f88d2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f88d2-144">System.Boolean</span></span>

## <span data-ttu-id="f88d2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f88d2-145">NOTES</span></span>

## <span data-ttu-id="f88d2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f88d2-146">RELATED LINKS</span></span>
