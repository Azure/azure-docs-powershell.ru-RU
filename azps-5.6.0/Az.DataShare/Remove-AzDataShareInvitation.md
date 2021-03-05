---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 4736a1b6e8d0a6d34cf1874868596d4139ad5e67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996680"
---
# <span data-ttu-id="bd103-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bd103-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="bd103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd103-102">SYNOPSIS</span></span>
<span data-ttu-id="bd103-103">удаляет приглашение</span><span class="sxs-lookup"><span data-stu-id="bd103-103">removes an invitation</span></span>

## <span data-ttu-id="bd103-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd103-104">SYNTAX</span></span>

### <span data-ttu-id="bd103-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd103-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd103-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd103-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd103-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd103-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd103-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd103-108">DESCRIPTION</span></span>
<span data-ttu-id="bd103-109">При этом приглашение на удаление из области данных удаляется из-за начертания **AzDataShareInvitation.**</span><span class="sxs-lookup"><span data-stu-id="bd103-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="bd103-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd103-110">EXAMPLES</span></span>

### <span data-ttu-id="bd103-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd103-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bd103-112">Эти команды удаляют приглашение ADSInvite из share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="bd103-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="bd103-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd103-113">PARAMETERS</span></span>

### <span data-ttu-id="bd103-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd103-114">-AccountName</span></span>
<span data-ttu-id="bd103-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="bd103-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd103-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd103-116">-DefaultProfile</span></span>
<span data-ttu-id="bd103-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd103-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd103-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd103-118">-InputObject</span></span>
<span data-ttu-id="bd103-119">Объект приглашения на совместное использование данных Azure</span><span class="sxs-lookup"><span data-stu-id="bd103-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd103-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bd103-120">-Name</span></span>
<span data-ttu-id="bd103-121">Имя приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="bd103-121">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd103-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd103-122">-PassThru</span></span>
<span data-ttu-id="bd103-123">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="bd103-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="bd103-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd103-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd103-125">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="bd103-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd103-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd103-126">-ResourceId</span></span>
<span data-ttu-id="bd103-127">ИД ресурса приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="bd103-127">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd103-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bd103-128">-ShareName</span></span>
<span data-ttu-id="bd103-129">Имя обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="bd103-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd103-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd103-130">-Confirm</span></span>
<span data-ttu-id="bd103-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd103-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd103-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd103-132">-WhatIf</span></span>
<span data-ttu-id="bd103-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd103-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd103-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd103-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd103-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd103-135">CommonParameters</span></span>
<span data-ttu-id="bd103-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd103-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd103-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd103-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd103-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd103-138">INPUTS</span></span>

### <span data-ttu-id="bd103-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bd103-139">System.String</span></span>

### <span data-ttu-id="bd103-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bd103-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="bd103-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd103-141">OUTPUTS</span></span>

### <span data-ttu-id="bd103-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd103-142">System.Boolean</span></span>

## <span data-ttu-id="bd103-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd103-143">NOTES</span></span>

## <span data-ttu-id="bd103-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd103-144">RELATED LINKS</span></span>
