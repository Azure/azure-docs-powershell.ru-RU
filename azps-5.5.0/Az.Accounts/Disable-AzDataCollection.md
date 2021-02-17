---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229524"
---
# <span data-ttu-id="22cfc-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="22cfc-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="22cfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="22cfc-103">Отказ от сбора данных для улучшения работы с azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="22cfc-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="22cfc-104">Данные собираются по умолчанию, если вы явным образом не откажетлись от них.</span><span class="sxs-lookup"><span data-stu-id="22cfc-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="22cfc-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22cfc-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cfc-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22cfc-106">DESCRIPTION</span></span>

<span data-ttu-id="22cfc-107">Этот `Disable-AzDataCollection` cmdlet используется для отказа от сбора данных.</span><span class="sxs-lookup"><span data-stu-id="22cfc-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="22cfc-108">Azure PowerShell по умолчанию автоматически собирает данные телеметрии.</span><span class="sxs-lookup"><span data-stu-id="22cfc-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="22cfc-109">Чтобы отключить сбор данных, необходимо явно отказаться от нее. Корпорация Майкрософт собирает собранные данные для выявления шаблонов использования, выявления распространенных проблем и улучшения работы Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="22cfc-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="22cfc-110">Microsoft Azure PowerShell не собирает личные или личные данные.</span><span class="sxs-lookup"><span data-stu-id="22cfc-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="22cfc-111">Если вы ранее решили отказаться от нее, запустите этот cmdlet, чтобы повторно включить сбор данных для текущего пользователя `Enable-AzDataCollection` на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="22cfc-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="22cfc-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22cfc-112">EXAMPLES</span></span>

### <span data-ttu-id="22cfc-113">Пример 1. Отключение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="22cfc-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="22cfc-114">В следующем примере показано, как отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="22cfc-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="22cfc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cfc-115">PARAMETERS</span></span>

### <span data-ttu-id="22cfc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cfc-116">-DefaultProfile</span></span>

<span data-ttu-id="22cfc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22cfc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cfc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22cfc-118">-Confirm</span></span>

<span data-ttu-id="22cfc-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="22cfc-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cfc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cfc-120">-WhatIf</span></span>

<span data-ttu-id="22cfc-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22cfc-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22cfc-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22cfc-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cfc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cfc-123">CommonParameters</span></span>

<span data-ttu-id="22cfc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cfc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cfc-125">Дополнительные сведения см. [в about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="22cfc-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="22cfc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22cfc-126">INPUTS</span></span>

### <span data-ttu-id="22cfc-127">Нет</span><span class="sxs-lookup"><span data-stu-id="22cfc-127">None</span></span>

## <span data-ttu-id="22cfc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22cfc-128">OUTPUTS</span></span>

### <span data-ttu-id="22cfc-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="22cfc-129">System.Void</span></span>

## <span data-ttu-id="22cfc-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22cfc-130">NOTES</span></span>

## <span data-ttu-id="22cfc-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22cfc-131">RELATED LINKS</span></span>

[<span data-ttu-id="22cfc-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="22cfc-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
