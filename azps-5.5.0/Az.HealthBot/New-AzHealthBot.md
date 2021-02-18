---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: dc39a7324f89e0a45efd4b631fb24a2e000d5e72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214644"
---
# <span data-ttu-id="737dd-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="737dd-101">New-AzHealthBot</span></span>

## <span data-ttu-id="737dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737dd-102">SYNOPSIS</span></span>
<span data-ttu-id="737dd-103">Создайте нового бота HealthBot.</span><span class="sxs-lookup"><span data-stu-id="737dd-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="737dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="737dd-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="737dd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="737dd-105">DESCRIPTION</span></span>
<span data-ttu-id="737dd-106">Создайте нового бота HealthBot.</span><span class="sxs-lookup"><span data-stu-id="737dd-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="737dd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="737dd-107">EXAMPLES</span></span>

### <span data-ttu-id="737dd-108">Пример 1. Создание нового бота HealthBot</span><span class="sxs-lookup"><span data-stu-id="737dd-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="737dd-109">Создание нового бота по умолчанию</span><span class="sxs-lookup"><span data-stu-id="737dd-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="737dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="737dd-110">PARAMETERS</span></span>

### <span data-ttu-id="737dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="737dd-111">-AsJob</span></span>
<span data-ttu-id="737dd-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="737dd-112">Run the command as a job</span></span>

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

### <span data-ttu-id="737dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737dd-113">-DefaultProfile</span></span>
<span data-ttu-id="737dd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="737dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737dd-115">-Location</span><span class="sxs-lookup"><span data-stu-id="737dd-115">-Location</span></span>
<span data-ttu-id="737dd-116">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="737dd-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="737dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="737dd-117">-Name</span></span>
<span data-ttu-id="737dd-118">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="737dd-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737dd-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="737dd-119">-NoWait</span></span>
<span data-ttu-id="737dd-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="737dd-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="737dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="737dd-122">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="737dd-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="737dd-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="737dd-123">-Sku</span></span>
<span data-ttu-id="737dd-124">Имя SKU HealthBot</span><span class="sxs-lookup"><span data-stu-id="737dd-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737dd-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="737dd-125">-SubscriptionId</span></span>
<span data-ttu-id="737dd-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="737dd-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="737dd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="737dd-127">-Tag</span></span>
<span data-ttu-id="737dd-128">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="737dd-128">Resource tags.</span></span>

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

### <span data-ttu-id="737dd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="737dd-129">-Confirm</span></span>
<span data-ttu-id="737dd-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737dd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737dd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737dd-131">-WhatIf</span></span>
<span data-ttu-id="737dd-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737dd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="737dd-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="737dd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737dd-134">CommonParameters</span></span>
<span data-ttu-id="737dd-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737dd-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="737dd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737dd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="737dd-137">INPUTS</span></span>

## <span data-ttu-id="737dd-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="737dd-138">OUTPUTS</span></span>

### <span data-ttu-id="737dd-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="737dd-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="737dd-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="737dd-140">NOTES</span></span>

<span data-ttu-id="737dd-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="737dd-141">ALIASES</span></span>

## <span data-ttu-id="737dd-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="737dd-142">RELATED LINKS</span></span>

