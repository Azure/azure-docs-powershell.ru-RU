---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: c0b2b8eb249e466c0e57127e0df9ee9b0afad048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721181"
---
# <span data-ttu-id="46e6e-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="46e6e-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="46e6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="46e6e-103">Создание новой учетной записи для общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="46e6e-103">Creates new data share account</span></span>

## <span data-ttu-id="46e6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46e6e-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e6e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e6e-105">DESCRIPTION</span></span>
<span data-ttu-id="46e6e-106">Командлет **New-AzDataShareAccount** создает учетную запись для общего доступа к данным в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6e-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="46e6e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46e6e-107">EXAMPLES</span></span>

### <span data-ttu-id="46e6e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46e6e-108">Example 1</span></span>
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

<span data-ttu-id="46e6e-109">Создание учетной записи с именем "WikiADS" в группе ресурсов "ADS"</span><span class="sxs-lookup"><span data-stu-id="46e6e-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="46e6e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46e6e-110">PARAMETERS</span></span>

### <span data-ttu-id="46e6e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46e6e-111">-AsJob</span></span>
<span data-ttu-id="46e6e-112">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="46e6e-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="46e6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e6e-113">-DefaultProfile</span></span>
<span data-ttu-id="46e6e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e6e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="46e6e-115">-Location</span></span>
<span data-ttu-id="46e6e-116">Расположение, в котором нужно создать учетную запись для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="46e6e-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="46e6e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46e6e-117">-Name</span></span>
<span data-ttu-id="46e6e-118">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6e-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="46e6e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e6e-119">-ResourceGroupName</span></span>
<span data-ttu-id="46e6e-120">Имя группы ресурсов для учетной записи общего доступа к данным Azure будет создано в.</span><span class="sxs-lookup"><span data-stu-id="46e6e-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="46e6e-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="46e6e-121">-Tag</span></span>
<span data-ttu-id="46e6e-122">Теги, которые нужно связать с учетной записью общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6e-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="46e6e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46e6e-123">-Confirm</span></span>
<span data-ttu-id="46e6e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="46e6e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e6e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e6e-125">-WhatIf</span></span>
<span data-ttu-id="46e6e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="46e6e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e6e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="46e6e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e6e-128">CommonParameters</span></span>
<span data-ttu-id="46e6e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46e6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e6e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e6e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e6e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46e6e-131">INPUTS</span></span>

### <span data-ttu-id="46e6e-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="46e6e-132">None</span></span>

## <span data-ttu-id="46e6e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e6e-133">OUTPUTS</span></span>

### <span data-ttu-id="46e6e-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="46e6e-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="46e6e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="46e6e-135">NOTES</span></span>

## <span data-ttu-id="46e6e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46e6e-136">RELATED LINKS</span></span>
