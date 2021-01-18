---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505141"
---
# <span data-ttu-id="a6890-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a6890-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="a6890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6890-102">SYNOPSIS</span></span>
<span data-ttu-id="a6890-103">Удалите службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a6890-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="a6890-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6890-104">SYNTAX</span></span>

### <span data-ttu-id="a6890-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6890-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6890-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6890-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6890-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6890-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6890-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6890-108">DESCRIPTION</span></span>
<span data-ttu-id="a6890-109">С **помощью cmdlet Remove-AzSearchService** удаляется служба Azure Search с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="a6890-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="a6890-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6890-110">EXAMPLES</span></span>

### <span data-ttu-id="a6890-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6890-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="a6890-112">В этом примере удаляется служба поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a6890-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="a6890-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6890-113">PARAMETERS</span></span>

### <span data-ttu-id="a6890-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6890-114">-DefaultProfile</span></span>
<span data-ttu-id="a6890-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6890-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6890-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a6890-116">-Force</span></span>
<span data-ttu-id="a6890-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a6890-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6890-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6890-118">-InputObject</span></span>
<span data-ttu-id="a6890-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="a6890-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6890-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a6890-120">-Name</span></span>
<span data-ttu-id="a6890-121">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="a6890-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6890-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6890-122">-PassThru</span></span>
<span data-ttu-id="a6890-123">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6890-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a6890-124">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="a6890-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a6890-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6890-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6890-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6890-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6890-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6890-127">-ResourceId</span></span>
<span data-ttu-id="a6890-128">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="a6890-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6890-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6890-129">-Confirm</span></span>
<span data-ttu-id="a6890-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a6890-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6890-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6890-131">-WhatIf</span></span>
<span data-ttu-id="a6890-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6890-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6890-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6890-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6890-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6890-134">CommonParameters</span></span>
<span data-ttu-id="a6890-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6890-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6890-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6890-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6890-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6890-137">INPUTS</span></span>

### <span data-ttu-id="a6890-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a6890-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a6890-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a6890-139">System.String</span></span>

## <span data-ttu-id="a6890-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6890-140">OUTPUTS</span></span>

### <span data-ttu-id="a6890-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6890-141">System.Boolean</span></span>

## <span data-ttu-id="a6890-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6890-142">NOTES</span></span>

## <span data-ttu-id="a6890-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6890-143">RELATED LINKS</span></span>

[<span data-ttu-id="a6890-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a6890-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="a6890-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a6890-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="a6890-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a6890-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

