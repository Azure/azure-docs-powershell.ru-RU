---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393263"
---
# <span data-ttu-id="d78d1-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d78d1-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="d78d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d78d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d78d1-103">Позволяет Azure PowerShell собирать данные для улучшения пользовательского интерфейса с помощью cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d78d1-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d78d1-104">При выполнении этого cmdlet выполняется сбор данных текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="d78d1-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="d78d1-105">Данные собираются по умолчанию, если вы явным образом не откажетлись от них.</span><span class="sxs-lookup"><span data-stu-id="d78d1-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="d78d1-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d78d1-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d78d1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d78d1-107">DESCRIPTION</span></span>

<span data-ttu-id="d78d1-108">Этот `Enable-AzDataCollection` cmdlet используется для использования сбора данных.</span><span class="sxs-lookup"><span data-stu-id="d78d1-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="d78d1-109">Azure PowerShell по умолчанию автоматически собирает данные телеметрии.</span><span class="sxs-lookup"><span data-stu-id="d78d1-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="d78d1-110">Корпорация Майкрософт собирает собранные данные для выявления шаблонов использования, выявления распространенных проблем и улучшения работы Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d78d1-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="d78d1-111">Microsoft Azure PowerShell не собирает личные или личные данные.</span><span class="sxs-lookup"><span data-stu-id="d78d1-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="d78d1-112">Чтобы отключить сбор данных, необходимо явно отказаться от нее путем выполнения `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="d78d1-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="d78d1-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d78d1-113">EXAMPLES</span></span>

### <span data-ttu-id="d78d1-114">Пример 1. Включение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="d78d1-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="d78d1-115">В следующем примере показано, как включить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d78d1-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="d78d1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d78d1-116">PARAMETERS</span></span>

### <span data-ttu-id="d78d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78d1-117">-DefaultProfile</span></span>

<span data-ttu-id="d78d1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d78d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d78d1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d78d1-119">-Confirm</span></span>

<span data-ttu-id="d78d1-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d78d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d78d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d78d1-121">-WhatIf</span></span>

<span data-ttu-id="d78d1-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d78d1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d78d1-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d78d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d78d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78d1-124">CommonParameters</span></span>

<span data-ttu-id="d78d1-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78d1-126">Дополнительные сведения см. [в about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="d78d1-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="d78d1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d78d1-127">INPUTS</span></span>

### <span data-ttu-id="d78d1-128">Нет</span><span class="sxs-lookup"><span data-stu-id="d78d1-128">None</span></span>

## <span data-ttu-id="d78d1-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d78d1-129">OUTPUTS</span></span>

### <span data-ttu-id="d78d1-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d78d1-130">System.Void</span></span>

## <span data-ttu-id="d78d1-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d78d1-131">NOTES</span></span>

## <span data-ttu-id="d78d1-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d78d1-132">RELATED LINKS</span></span>

[<span data-ttu-id="d78d1-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d78d1-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
