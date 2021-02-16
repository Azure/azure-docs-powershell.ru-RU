---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212004"
---
# <span data-ttu-id="47964-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="47964-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="47964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47964-102">SYNOPSIS</span></span>
<span data-ttu-id="47964-103">Чтобы проверить, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="47964-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="47964-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47964-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47964-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47964-105">DESCRIPTION</span></span>
<span data-ttu-id="47964-106">Чтобы проверить, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="47964-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="47964-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47964-107">EXAMPLES</span></span>

### <span data-ttu-id="47964-108">Пример 1. Проверка на наличии имени ресурса</span><span class="sxs-lookup"><span data-stu-id="47964-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="47964-109">Команда проверяет, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="47964-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="47964-110">Пример 2. Проверка на наличии имени ресурса</span><span class="sxs-lookup"><span data-stu-id="47964-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="47964-111">Команда проверяет, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="47964-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="47964-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47964-112">PARAMETERS</span></span>

### <span data-ttu-id="47964-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47964-113">-DefaultProfile</span></span>
<span data-ttu-id="47964-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47964-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47964-115">-Location</span><span class="sxs-lookup"><span data-stu-id="47964-115">-Location</span></span>
<span data-ttu-id="47964-116">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="47964-116">Location Name.</span></span>

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

### <span data-ttu-id="47964-117">-Name</span><span class="sxs-lookup"><span data-stu-id="47964-117">-Name</span></span>
<span data-ttu-id="47964-118">Возвращает или устанавливает проверяемую фамилию.</span><span class="sxs-lookup"><span data-stu-id="47964-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="47964-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47964-119">-SubscriptionId</span></span>
<span data-ttu-id="47964-120">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47964-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47964-121">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="47964-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47964-122">-Type</span><span class="sxs-lookup"><span data-stu-id="47964-122">-Type</span></span>
<span data-ttu-id="47964-123">Возвращает или задает тип проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="47964-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="47964-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47964-124">-Confirm</span></span>
<span data-ttu-id="47964-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47964-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47964-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47964-126">-WhatIf</span></span>
<span data-ttu-id="47964-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47964-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47964-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47964-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47964-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47964-129">CommonParameters</span></span>
<span data-ttu-id="47964-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47964-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47964-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47964-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47964-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47964-132">INPUTS</span></span>

## <span data-ttu-id="47964-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47964-133">OUTPUTS</span></span>

### <span data-ttu-id="47964-134">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="47964-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="47964-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47964-135">NOTES</span></span>

<span data-ttu-id="47964-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47964-136">ALIASES</span></span>

## <span data-ttu-id="47964-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47964-137">RELATED LINKS</span></span>

