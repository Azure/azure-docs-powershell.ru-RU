---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999043"
---
# <span data-ttu-id="64a2f-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="64a2f-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="64a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="64a2f-103">Позволяет Azure PowerShell собирать данные для улучшения пользовательского интерфейса с помощью cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64a2f-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="64a2f-104">При выполнении этого cmdlet выполняется сбор данных текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="64a2f-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="64a2f-105">Данные собираются по умолчанию, если вы явным образом не откажетлись от них.</span><span class="sxs-lookup"><span data-stu-id="64a2f-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="64a2f-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64a2f-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a2f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64a2f-107">DESCRIPTION</span></span>

<span data-ttu-id="64a2f-108">Этот `Enable-AzDataCollection` cmdlet используется для использования сбора данных.</span><span class="sxs-lookup"><span data-stu-id="64a2f-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="64a2f-109">Azure PowerShell по умолчанию автоматически собирает данные телеметрии.</span><span class="sxs-lookup"><span data-stu-id="64a2f-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="64a2f-110">Корпорация Майкрософт собирает собранные данные для выявления шаблонов использования, выявления распространенных проблем и улучшения работы Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64a2f-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="64a2f-111">Microsoft Azure PowerShell не собирает личные или личные данные.</span><span class="sxs-lookup"><span data-stu-id="64a2f-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="64a2f-112">Чтобы отключить сбор данных, необходимо явно отказаться от нее путем `Disable-AzDataCollection` выполнения.</span><span class="sxs-lookup"><span data-stu-id="64a2f-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="64a2f-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64a2f-113">EXAMPLES</span></span>

### <span data-ttu-id="64a2f-114">Пример 1. Включение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="64a2f-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="64a2f-115">В следующем примере показано, как включить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="64a2f-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="64a2f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a2f-116">PARAMETERS</span></span>

### <span data-ttu-id="64a2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a2f-117">-DefaultProfile</span></span>

<span data-ttu-id="64a2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64a2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a2f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64a2f-119">-Confirm</span></span>

<span data-ttu-id="64a2f-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a2f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a2f-121">-WhatIf</span></span>

<span data-ttu-id="64a2f-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a2f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64a2f-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64a2f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a2f-124">CommonParameters</span></span>
<span data-ttu-id="64a2f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a2f-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64a2f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a2f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64a2f-127">INPUTS</span></span>

### <span data-ttu-id="64a2f-128">Нет</span><span class="sxs-lookup"><span data-stu-id="64a2f-128">None</span></span>

## <span data-ttu-id="64a2f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64a2f-129">OUTPUTS</span></span>

### <span data-ttu-id="64a2f-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="64a2f-130">System.Void</span></span>

## <span data-ttu-id="64a2f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64a2f-131">NOTES</span></span>

## <span data-ttu-id="64a2f-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64a2f-132">RELATED LINKS</span></span>

[<span data-ttu-id="64a2f-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="64a2f-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
