---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240349"
---
# <span data-ttu-id="91876-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="91876-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="91876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91876-102">SYNOPSIS</span></span>
<span data-ttu-id="91876-103">Удаление зарегистрированного префикса из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="91876-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="91876-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91876-104">SYNTAX</span></span>

### <span data-ttu-id="91876-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91876-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91876-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="91876-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91876-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91876-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91876-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91876-108">DESCRIPTION</span></span>
<span data-ttu-id="91876-109">Позволяет удалить зарегистрированный префикс из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="91876-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="91876-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91876-110">EXAMPLES</span></span>

### <span data-ttu-id="91876-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91876-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="91876-112">Удаление зарегистрированного префикса по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="91876-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="91876-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91876-113">PARAMETERS</span></span>

### <span data-ttu-id="91876-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91876-114">-AsJob</span></span>
<span data-ttu-id="91876-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="91876-115">Run in the background.</span></span>

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

### <span data-ttu-id="91876-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91876-116">-DefaultProfile</span></span>
<span data-ttu-id="91876-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91876-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91876-118">-Force</span><span class="sxs-lookup"><span data-stu-id="91876-118">-Force</span></span>
<span data-ttu-id="91876-119">Принудительное завершение операции</span><span class="sxs-lookup"><span data-stu-id="91876-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="91876-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91876-120">-InputObject</span></span>
<span data-ttu-id="91876-121">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="91876-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="91876-122">-Name</span><span class="sxs-lookup"><span data-stu-id="91876-122">-Name</span></span>
<span data-ttu-id="91876-123">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="91876-123">The name of prefix.</span></span>

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

### <span data-ttu-id="91876-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91876-124">-PassThru</span></span>
<span data-ttu-id="91876-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="91876-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="91876-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="91876-126">-PeeringName</span></span>
<span data-ttu-id="91876-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="91876-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="91876-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91876-128">-ResourceGroupName</span></span>
<span data-ttu-id="91876-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91876-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="91876-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91876-130">-ResourceId</span></span>
<span data-ttu-id="91876-131">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="91876-131">The resource id string name.</span></span>

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

### <span data-ttu-id="91876-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91876-132">-Confirm</span></span>
<span data-ttu-id="91876-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91876-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91876-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91876-134">-WhatIf</span></span>
<span data-ttu-id="91876-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91876-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91876-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91876-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91876-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91876-137">CommonParameters</span></span>
<span data-ttu-id="91876-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91876-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91876-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91876-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91876-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91876-140">INPUTS</span></span>

### <span data-ttu-id="91876-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="91876-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="91876-142">System.String</span><span class="sxs-lookup"><span data-stu-id="91876-142">System.String</span></span>

## <span data-ttu-id="91876-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91876-143">OUTPUTS</span></span>

### <span data-ttu-id="91876-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91876-144">System.Boolean</span></span>

## <span data-ttu-id="91876-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91876-145">NOTES</span></span>

## <span data-ttu-id="91876-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91876-146">RELATED LINKS</span></span>
