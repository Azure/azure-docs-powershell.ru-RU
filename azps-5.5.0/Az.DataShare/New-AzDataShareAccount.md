---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220164"
---
# <span data-ttu-id="81bd0-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="81bd0-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="81bd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="81bd0-103">Создание учетной записи для обмена данными</span><span class="sxs-lookup"><span data-stu-id="81bd0-103">Creates new data share account</span></span>

## <span data-ttu-id="81bd0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81bd0-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81bd0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="81bd0-106">**Новый-AzDataShareAccount** создает учетную запись datashare в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="81bd0-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="81bd0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="81bd0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81bd0-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="81bd0-109">Создает учетную запись с именем "WikiADS" в группе ресурсов "ADS"</span><span class="sxs-lookup"><span data-stu-id="81bd0-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="81bd0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="81bd0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81bd0-111">-AsJob</span></span>
<span data-ttu-id="81bd0-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="81bd0-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="81bd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bd0-113">-DefaultProfile</span></span>
<span data-ttu-id="81bd0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81bd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81bd0-115">-Location</span><span class="sxs-lookup"><span data-stu-id="81bd0-115">-Location</span></span>
<span data-ttu-id="81bd0-116">Расположение, в котором нужно создать учетную запись для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="81bd0-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bd0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="81bd0-117">-Name</span></span>
<span data-ttu-id="81bd0-118">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="81bd0-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bd0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bd0-119">-ResourceGroupName</span></span>
<span data-ttu-id="81bd0-120">Имя группы ресурсов учетной записи azure data share будет создано в.</span><span class="sxs-lookup"><span data-stu-id="81bd0-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bd0-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="81bd0-121">-Tag</span></span>
<span data-ttu-id="81bd0-122">Теги, которые нужно связать с учетной записью azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="81bd0-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bd0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81bd0-123">-Confirm</span></span>
<span data-ttu-id="81bd0-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="81bd0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81bd0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bd0-125">-WhatIf</span></span>
<span data-ttu-id="81bd0-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81bd0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81bd0-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81bd0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81bd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bd0-128">CommonParameters</span></span>
<span data-ttu-id="81bd0-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81bd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bd0-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81bd0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bd0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81bd0-131">INPUTS</span></span>

### <span data-ttu-id="81bd0-132">Нет</span><span class="sxs-lookup"><span data-stu-id="81bd0-132">None</span></span>

## <span data-ttu-id="81bd0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81bd0-133">OUTPUTS</span></span>

### <span data-ttu-id="81bd0-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="81bd0-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="81bd0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81bd0-135">NOTES</span></span>

## <span data-ttu-id="81bd0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81bd0-136">RELATED LINKS</span></span>
