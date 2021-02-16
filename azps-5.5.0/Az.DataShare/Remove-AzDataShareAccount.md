---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214892"
---
# <span data-ttu-id="1cf22-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="1cf22-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="1cf22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cf22-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf22-103">Удаление учетной записи datashare</span><span class="sxs-lookup"><span data-stu-id="1cf22-103">Removes a datashare account</span></span>

## <span data-ttu-id="1cf22-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cf22-104">SYNTAX</span></span>

### <span data-ttu-id="1cf22-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cf22-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf22-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf22-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf22-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf22-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cf22-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cf22-108">DESCRIPTION</span></span>
<span data-ttu-id="1cf22-109">Для **удаления учетной записи datashare удаляется cmdlet Remove-AzDataShareAccount.**</span><span class="sxs-lookup"><span data-stu-id="1cf22-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="1cf22-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cf22-110">EXAMPLES</span></span>

### <span data-ttu-id="1cf22-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cf22-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1cf22-112">Эта команда удаляет учетную запись datashare с именем WikiADS из группы ресурсов ADS.</span><span class="sxs-lookup"><span data-stu-id="1cf22-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="1cf22-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="1cf22-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1cf22-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cf22-114">PARAMETERS</span></span>

### <span data-ttu-id="1cf22-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cf22-115">-AsJob</span></span>
<span data-ttu-id="1cf22-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="1cf22-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="1cf22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf22-117">-DefaultProfile</span></span>
<span data-ttu-id="1cf22-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cf22-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1cf22-119">-Force</span></span>
<span data-ttu-id="1cf22-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="1cf22-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="1cf22-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cf22-121">-InputObject</span></span>
<span data-ttu-id="1cf22-122">Объект учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf22-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf22-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1cf22-123">-Name</span></span>
<span data-ttu-id="1cf22-124">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf22-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="1cf22-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cf22-125">-PassThru</span></span>
<span data-ttu-id="1cf22-126">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="1cf22-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="1cf22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf22-127">-ResourceGroupName</span></span>
<span data-ttu-id="1cf22-128">Имя группы ресурсов учетной записи обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf22-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="1cf22-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cf22-129">-ResourceId</span></span>
<span data-ttu-id="1cf22-130">ИД ресурса учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="1cf22-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="1cf22-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cf22-131">-Confirm</span></span>
<span data-ttu-id="1cf22-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1cf22-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cf22-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf22-133">-WhatIf</span></span>
<span data-ttu-id="1cf22-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cf22-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cf22-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1cf22-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cf22-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf22-136">CommonParameters</span></span>
<span data-ttu-id="1cf22-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cf22-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf22-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cf22-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf22-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cf22-139">INPUTS</span></span>

### <span data-ttu-id="1cf22-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1cf22-140">System.String</span></span>

### <span data-ttu-id="1cf22-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="1cf22-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="1cf22-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cf22-142">OUTPUTS</span></span>

### <span data-ttu-id="1cf22-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cf22-143">System.Boolean</span></span>

## <span data-ttu-id="1cf22-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cf22-144">NOTES</span></span>

## <span data-ttu-id="1cf22-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cf22-145">RELATED LINKS</span></span>
