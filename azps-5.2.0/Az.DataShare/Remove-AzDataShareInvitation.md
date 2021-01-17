---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407959"
---
# <span data-ttu-id="71418-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="71418-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="71418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71418-102">SYNOPSIS</span></span>
<span data-ttu-id="71418-103">удаляет приглашение</span><span class="sxs-lookup"><span data-stu-id="71418-103">removes an invitation</span></span>

## <span data-ttu-id="71418-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71418-104">SYNTAX</span></span>

### <span data-ttu-id="71418-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71418-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71418-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71418-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71418-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71418-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71418-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71418-108">DESCRIPTION</span></span>
<span data-ttu-id="71418-109">При этом приглашение на удаление из области данных удаляется из-за начертания **AzDataShareInvitation.**</span><span class="sxs-lookup"><span data-stu-id="71418-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="71418-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71418-110">EXAMPLES</span></span>

### <span data-ttu-id="71418-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71418-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="71418-112">Эти команды удаляют приглашение ADSInvite из share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="71418-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="71418-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71418-113">PARAMETERS</span></span>

### <span data-ttu-id="71418-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71418-114">-AccountName</span></span>
<span data-ttu-id="71418-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="71418-115">Azure data share account name</span></span>

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

### <span data-ttu-id="71418-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71418-116">-DefaultProfile</span></span>
<span data-ttu-id="71418-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71418-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71418-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71418-118">-InputObject</span></span>
<span data-ttu-id="71418-119">Объект приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="71418-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="71418-120">-Name</span><span class="sxs-lookup"><span data-stu-id="71418-120">-Name</span></span>
<span data-ttu-id="71418-121">Имя приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="71418-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="71418-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71418-122">-PassThru</span></span>
<span data-ttu-id="71418-123">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="71418-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="71418-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71418-124">-ResourceGroupName</span></span>
<span data-ttu-id="71418-125">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="71418-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="71418-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71418-126">-ResourceId</span></span>
<span data-ttu-id="71418-127">ИД ресурса приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="71418-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="71418-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="71418-128">-ShareName</span></span>
<span data-ttu-id="71418-129">Имя обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="71418-129">Azure data share name.</span></span>

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

### <span data-ttu-id="71418-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71418-130">-Confirm</span></span>
<span data-ttu-id="71418-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71418-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71418-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71418-132">-WhatIf</span></span>
<span data-ttu-id="71418-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71418-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71418-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71418-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71418-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71418-135">CommonParameters</span></span>
<span data-ttu-id="71418-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71418-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71418-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71418-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71418-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71418-138">INPUTS</span></span>

### <span data-ttu-id="71418-139">System.String</span><span class="sxs-lookup"><span data-stu-id="71418-139">System.String</span></span>

### <span data-ttu-id="71418-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="71418-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="71418-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71418-141">OUTPUTS</span></span>

### <span data-ttu-id="71418-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71418-142">System.Boolean</span></span>

## <span data-ttu-id="71418-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71418-143">NOTES</span></span>

## <span data-ttu-id="71418-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71418-144">RELATED LINKS</span></span>
