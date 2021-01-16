---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424876"
---
# <span data-ttu-id="e7b30-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="e7b30-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="e7b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b30-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b30-103">Удаление зарегистрированного ASN из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="e7b30-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="e7b30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7b30-104">SYNTAX</span></span>

### <span data-ttu-id="e7b30-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7b30-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7b30-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e7b30-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7b30-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b30-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7b30-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7b30-108">DESCRIPTION</span></span>
<span data-ttu-id="e7b30-109">Позволяет удалить зарегистрированные ASN из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="e7b30-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="e7b30-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7b30-110">EXAMPLES</span></span>

### <span data-ttu-id="e7b30-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7b30-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="e7b30-112">Удаление зарегистрированного asN по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="e7b30-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="e7b30-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7b30-113">PARAMETERS</span></span>

### <span data-ttu-id="e7b30-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7b30-114">-AsJob</span></span>
<span data-ttu-id="e7b30-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="e7b30-115">Run in the background.</span></span>

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

### <span data-ttu-id="e7b30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b30-116">-DefaultProfile</span></span>
<span data-ttu-id="e7b30-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7b30-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e7b30-118">-Force</span></span>
<span data-ttu-id="e7b30-119">Принудительное завершение операции</span><span class="sxs-lookup"><span data-stu-id="e7b30-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="e7b30-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7b30-120">-InputObject</span></span>
<span data-ttu-id="e7b30-121">Использование Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e7b30-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="e7b30-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e7b30-122">-Name</span></span>
<span data-ttu-id="e7b30-123">Имя зарегистрированного asN</span><span class="sxs-lookup"><span data-stu-id="e7b30-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="e7b30-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7b30-124">-PassThru</span></span>
<span data-ttu-id="e7b30-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e7b30-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e7b30-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e7b30-126">-PeeringName</span></span>
<span data-ttu-id="e7b30-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e7b30-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e7b30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b30-128">-ResourceGroupName</span></span>
<span data-ttu-id="e7b30-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7b30-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e7b30-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b30-130">-ResourceId</span></span>
<span data-ttu-id="e7b30-131">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="e7b30-131">The resource id string name.</span></span>

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

### <span data-ttu-id="e7b30-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7b30-132">-Confirm</span></span>
<span data-ttu-id="e7b30-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b30-134">-WhatIf</span></span>
<span data-ttu-id="e7b30-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b30-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e7b30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b30-137">CommonParameters</span></span>
<span data-ttu-id="e7b30-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b30-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7b30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b30-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7b30-140">INPUTS</span></span>

### <span data-ttu-id="e7b30-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e7b30-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="e7b30-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e7b30-142">System.String</span></span>

## <span data-ttu-id="e7b30-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7b30-143">OUTPUTS</span></span>

### <span data-ttu-id="e7b30-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7b30-144">System.Boolean</span></span>

## <span data-ttu-id="e7b30-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7b30-145">NOTES</span></span>

## <span data-ttu-id="e7b30-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7b30-146">RELATED LINKS</span></span>
