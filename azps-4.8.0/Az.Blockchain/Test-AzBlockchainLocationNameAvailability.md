---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243697"
---
# <span data-ttu-id="cd48e-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cd48e-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="cd48e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd48e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd48e-103">Чтобы проверить, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd48e-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="cd48e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd48e-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd48e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd48e-105">DESCRIPTION</span></span>
<span data-ttu-id="cd48e-106">Чтобы проверить, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd48e-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="cd48e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd48e-107">EXAMPLES</span></span>

### <span data-ttu-id="cd48e-108">Пример 1: Проверка наличия имени ресурса</span><span class="sxs-lookup"><span data-stu-id="cd48e-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="cd48e-109">Команда проверяет, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd48e-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="cd48e-110">Пример 2: Проверка наличия имени ресурса</span><span class="sxs-lookup"><span data-stu-id="cd48e-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="cd48e-111">Команда проверяет, доступно ли имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd48e-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="cd48e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd48e-112">PARAMETERS</span></span>

### <span data-ttu-id="cd48e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd48e-113">-DefaultProfile</span></span>
<span data-ttu-id="cd48e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd48e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd48e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="cd48e-115">-Location</span></span>
<span data-ttu-id="cd48e-116">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="cd48e-116">Location Name.</span></span>

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

### <span data-ttu-id="cd48e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd48e-117">-Name</span></span>
<span data-ttu-id="cd48e-118">Возвращает или задает имя для проверки.</span><span class="sxs-lookup"><span data-stu-id="cd48e-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="cd48e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd48e-119">-SubscriptionId</span></span>
<span data-ttu-id="cd48e-120">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd48e-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd48e-121">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cd48e-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd48e-122">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="cd48e-122">-Type</span></span>
<span data-ttu-id="cd48e-123">Возвращает или задает тип ресурса для проверки.</span><span class="sxs-lookup"><span data-stu-id="cd48e-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="cd48e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd48e-124">-Confirm</span></span>
<span data-ttu-id="cd48e-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd48e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd48e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd48e-126">-WhatIf</span></span>
<span data-ttu-id="cd48e-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd48e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd48e-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd48e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd48e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd48e-129">CommonParameters</span></span>
<span data-ttu-id="cd48e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd48e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd48e-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd48e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd48e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd48e-132">INPUTS</span></span>

## <span data-ttu-id="cd48e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd48e-133">OUTPUTS</span></span>

### <span data-ttu-id="cd48e-134">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="cd48e-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="cd48e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd48e-135">NOTES</span></span>

<span data-ttu-id="cd48e-136">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cd48e-136">ALIASES</span></span>

## <span data-ttu-id="cd48e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd48e-137">RELATED LINKS</span></span>

