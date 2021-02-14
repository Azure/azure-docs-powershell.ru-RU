---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228620"
---
# <span data-ttu-id="22e79-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="22e79-101">Set-AzDataShare</span></span>

## <span data-ttu-id="22e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e79-102">SYNOPSIS</span></span>
<span data-ttu-id="22e79-103">Обновление существующего обмена данными</span><span class="sxs-lookup"><span data-stu-id="22e79-103">Updates an existing data share</span></span>

## <span data-ttu-id="22e79-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22e79-104">SYNTAX</span></span>

### <span data-ttu-id="22e79-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22e79-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e79-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22e79-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e79-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22e79-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e79-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22e79-108">DESCRIPTION</span></span>
<span data-ttu-id="22e79-109">С **его использованием** обновляется объем данных, который существует в указанной учетной записи azure.</span><span class="sxs-lookup"><span data-stu-id="22e79-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="22e79-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22e79-110">EXAMPLES</span></span>

### <span data-ttu-id="22e79-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22e79-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="22e79-112">Эта команда обновляет существующий поделиться данными с именем AdsShare</span><span class="sxs-lookup"><span data-stu-id="22e79-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="22e79-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22e79-113">PARAMETERS</span></span>

### <span data-ttu-id="22e79-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22e79-114">-AccountName</span></span>
<span data-ttu-id="22e79-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="22e79-115">Azure data share account name</span></span>

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

### <span data-ttu-id="22e79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e79-116">-DefaultProfile</span></span>
<span data-ttu-id="22e79-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22e79-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e79-118">-Description</span><span class="sxs-lookup"><span data-stu-id="22e79-118">-Description</span></span>
<span data-ttu-id="22e79-119">Описание области "Поделиться данными"</span><span class="sxs-lookup"><span data-stu-id="22e79-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e79-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22e79-120">-InputObject</span></span>
<span data-ttu-id="22e79-121">Объект обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="22e79-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="22e79-122">-Name</span></span>
<span data-ttu-id="22e79-123">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="22e79-123">Azure data share name</span></span>

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

### <span data-ttu-id="22e79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e79-124">-ResourceGroupName</span></span>
<span data-ttu-id="22e79-125">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="22e79-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="22e79-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e79-126">-ResourceId</span></span>
<span data-ttu-id="22e79-127">ИД ресурса для azure data share</span><span class="sxs-lookup"><span data-stu-id="22e79-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="22e79-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="22e79-128">-TermsOfUse</span></span>
<span data-ttu-id="22e79-129">Условия использования для обмена данными</span><span class="sxs-lookup"><span data-stu-id="22e79-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e79-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22e79-130">-Confirm</span></span>
<span data-ttu-id="22e79-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22e79-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e79-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e79-132">-WhatIf</span></span>
<span data-ttu-id="22e79-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22e79-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22e79-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22e79-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e79-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e79-135">CommonParameters</span></span>
<span data-ttu-id="22e79-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e79-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e79-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22e79-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e79-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22e79-138">INPUTS</span></span>

### <span data-ttu-id="22e79-139">System.String</span><span class="sxs-lookup"><span data-stu-id="22e79-139">System.String</span></span>

### <span data-ttu-id="22e79-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="22e79-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="22e79-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22e79-141">OUTPUTS</span></span>

### <span data-ttu-id="22e79-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="22e79-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="22e79-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22e79-143">NOTES</span></span>

## <span data-ttu-id="22e79-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22e79-144">RELATED LINKS</span></span>
