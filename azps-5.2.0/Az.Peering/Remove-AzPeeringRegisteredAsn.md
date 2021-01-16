---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391671"
---
# <span data-ttu-id="3218c-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="3218c-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="3218c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3218c-102">SYNOPSIS</span></span>
<span data-ttu-id="3218c-103">Удаление зарегистрированного ASN из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="3218c-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="3218c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3218c-104">SYNTAX</span></span>

### <span data-ttu-id="3218c-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3218c-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3218c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3218c-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3218c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3218c-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3218c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3218c-108">DESCRIPTION</span></span>
<span data-ttu-id="3218c-109">Позволяет удалить зарегистрированные ASN из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="3218c-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="3218c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3218c-110">EXAMPLES</span></span>

### <span data-ttu-id="3218c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3218c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="3218c-112">Удаление зарегистрированного asN по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="3218c-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="3218c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3218c-113">PARAMETERS</span></span>

### <span data-ttu-id="3218c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3218c-114">-AsJob</span></span>
<span data-ttu-id="3218c-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="3218c-115">Run in the background.</span></span>

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

### <span data-ttu-id="3218c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3218c-116">-DefaultProfile</span></span>
<span data-ttu-id="3218c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3218c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3218c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3218c-118">-Force</span></span>
<span data-ttu-id="3218c-119">Принудительное завершение операции</span><span class="sxs-lookup"><span data-stu-id="3218c-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="3218c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3218c-120">-InputObject</span></span>
<span data-ttu-id="3218c-121">Использование Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3218c-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="3218c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3218c-122">-Name</span></span>
<span data-ttu-id="3218c-123">Имя зарегистрированного asN</span><span class="sxs-lookup"><span data-stu-id="3218c-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="3218c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3218c-124">-PassThru</span></span>
<span data-ttu-id="3218c-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="3218c-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3218c-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="3218c-126">-PeeringName</span></span>
<span data-ttu-id="3218c-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3218c-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="3218c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3218c-128">-ResourceGroupName</span></span>
<span data-ttu-id="3218c-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3218c-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="3218c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3218c-130">-ResourceId</span></span>
<span data-ttu-id="3218c-131">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="3218c-131">The resource id string name.</span></span>

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

### <span data-ttu-id="3218c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3218c-132">-Confirm</span></span>
<span data-ttu-id="3218c-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3218c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3218c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3218c-134">-WhatIf</span></span>
<span data-ttu-id="3218c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3218c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3218c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3218c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3218c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3218c-137">CommonParameters</span></span>
<span data-ttu-id="3218c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3218c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3218c-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3218c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3218c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3218c-140">INPUTS</span></span>

### <span data-ttu-id="3218c-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3218c-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="3218c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3218c-142">System.String</span></span>

## <span data-ttu-id="3218c-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3218c-143">OUTPUTS</span></span>

### <span data-ttu-id="3218c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3218c-144">System.Boolean</span></span>

## <span data-ttu-id="3218c-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3218c-145">NOTES</span></span>

## <span data-ttu-id="3218c-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3218c-146">RELATED LINKS</span></span>
