---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733344"
---
# <span data-ttu-id="beaf2-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="beaf2-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="beaf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="beaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="beaf2-103">Выбор подписки и учетной записи для назначения в командлетах PowerShell для Azure</span><span class="sxs-lookup"><span data-stu-id="beaf2-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beaf2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="beaf2-104">SYNTAX</span></span>

### <span data-ttu-id="beaf2-105">Объект input (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="beaf2-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beaf2-106">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="beaf2-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="beaf2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="beaf2-107">DESCRIPTION</span></span>
<span data-ttu-id="beaf2-108">Выберите подписку для назначения (или учетной записи или клиента) в командлетах Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="beaf2-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="beaf2-109">После этого командлета будущие командлеты будут ориентироваться на выбранный контекст.</span><span class="sxs-lookup"><span data-stu-id="beaf2-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="beaf2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="beaf2-110">EXAMPLES</span></span>

### <span data-ttu-id="beaf2-111">Пример 1: назначение именованного контекста</span><span class="sxs-lookup"><span data-stu-id="beaf2-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="beaf2-112">Назначение будущих командлетов PowerShell для Azure для учетной записи, клиента и подписки в контексте "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="beaf2-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="beaf2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="beaf2-113">PARAMETERS</span></span>

### <span data-ttu-id="beaf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaf2-114">-DefaultProfile</span></span>
<span data-ttu-id="beaf2-115">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="beaf2-115">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaf2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="beaf2-116">-InputObject</span></span>
<span data-ttu-id="beaf2-117">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="beaf2-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beaf2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="beaf2-118">-Name</span></span>
<span data-ttu-id="beaf2-119">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="beaf2-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaf2-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="beaf2-120">-Scope</span></span>
<span data-ttu-id="beaf2-121">Определяет область изменений контекста, например wheher изменения применяются только к процессу cusrrent или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="beaf2-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaf2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="beaf2-122">-Confirm</span></span>
<span data-ttu-id="beaf2-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="beaf2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beaf2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beaf2-124">-WhatIf</span></span>
<span data-ttu-id="beaf2-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="beaf2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beaf2-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="beaf2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beaf2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaf2-127">CommonParameters</span></span>
<span data-ttu-id="beaf2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="beaf2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaf2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beaf2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaf2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="beaf2-130">INPUTS</span></span>

### <span data-ttu-id="beaf2-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="beaf2-131">None</span></span>

## <span data-ttu-id="beaf2-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="beaf2-132">OUTPUTS</span></span>

### <span data-ttu-id="beaf2-133">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="beaf2-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="beaf2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="beaf2-134">NOTES</span></span>

## <span data-ttu-id="beaf2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="beaf2-135">RELATED LINKS</span></span>

