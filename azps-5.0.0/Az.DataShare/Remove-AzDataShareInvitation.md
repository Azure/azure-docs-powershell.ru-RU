---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312905"
---
# <span data-ttu-id="fb766-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="fb766-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="fb766-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb766-102">SYNOPSIS</span></span>
<span data-ttu-id="fb766-103">Удаление приглашения</span><span class="sxs-lookup"><span data-stu-id="fb766-103">removes an invitation</span></span>

## <span data-ttu-id="fb766-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb766-104">SYNTAX</span></span>

### <span data-ttu-id="fb766-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb766-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb766-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb766-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb766-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb766-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb766-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb766-108">DESCRIPTION</span></span>
<span data-ttu-id="fb766-109">Командлет **Remove-AzDataShareInvitation** удаляет приглашение на доступ к файлам.</span><span class="sxs-lookup"><span data-stu-id="fb766-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="fb766-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb766-110">EXAMPLES</span></span>

### <span data-ttu-id="fb766-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb766-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="fb766-112">Эта команда удаляет приглашение с именем ADSInvite из общего доступа AdsShare.</span><span class="sxs-lookup"><span data-stu-id="fb766-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="fb766-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb766-113">PARAMETERS</span></span>

### <span data-ttu-id="fb766-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="fb766-114">-AccountName</span></span>
<span data-ttu-id="fb766-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="fb766-115">Azure data share account name</span></span>

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

### <span data-ttu-id="fb766-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb766-116">-DefaultProfile</span></span>
<span data-ttu-id="fb766-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb766-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb766-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb766-118">-InputObject</span></span>
<span data-ttu-id="fb766-119">Объект приглашения на доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="fb766-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="fb766-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb766-120">-Name</span></span>
<span data-ttu-id="fb766-121">Имя приглашения на предоставление данных Azure</span><span class="sxs-lookup"><span data-stu-id="fb766-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="fb766-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb766-122">-PassThru</span></span>
<span data-ttu-id="fb766-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="fb766-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="fb766-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb766-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb766-125">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="fb766-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="fb766-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb766-126">-ResourceId</span></span>
<span data-ttu-id="fb766-127">Идентификатор ресурса для приглашения на доступ к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="fb766-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="fb766-128">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="fb766-128">-ShareName</span></span>
<span data-ttu-id="fb766-129">Имя общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="fb766-129">Azure data share name.</span></span>

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

### <span data-ttu-id="fb766-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb766-130">-Confirm</span></span>
<span data-ttu-id="fb766-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb766-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb766-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb766-132">-WhatIf</span></span>
<span data-ttu-id="fb766-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb766-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb766-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb766-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb766-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb766-135">CommonParameters</span></span>
<span data-ttu-id="fb766-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb766-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb766-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb766-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb766-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb766-138">INPUTS</span></span>

### <span data-ttu-id="fb766-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fb766-139">System.String</span></span>

### <span data-ttu-id="fb766-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="fb766-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="fb766-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb766-141">OUTPUTS</span></span>

### <span data-ttu-id="fb766-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb766-142">System.Boolean</span></span>

## <span data-ttu-id="fb766-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb766-143">NOTES</span></span>

## <span data-ttu-id="fb766-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb766-144">RELATED LINKS</span></span>
