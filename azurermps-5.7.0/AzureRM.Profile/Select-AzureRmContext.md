---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: c002db2d04905c19c3229a45feb9e00b5dc15754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567965"
---
# <span data-ttu-id="e62bb-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e62bb-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="e62bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e62bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e62bb-103">Выбор подписки и учетной записи для назначения в командлетах PowerShell для Azure</span><span class="sxs-lookup"><span data-stu-id="e62bb-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e62bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e62bb-104">SYNTAX</span></span>

### <span data-ttu-id="e62bb-105">SelectByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e62bb-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62bb-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="e62bb-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="e62bb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e62bb-107">DESCRIPTION</span></span>
<span data-ttu-id="e62bb-108">Выберите подписку для назначения (или учетной записи или клиента) в командлетах Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e62bb-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="e62bb-109">После этого командлета будущие командлеты будут ориентироваться на выбранный контекст.</span><span class="sxs-lookup"><span data-stu-id="e62bb-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="e62bb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e62bb-110">EXAMPLES</span></span>

### <span data-ttu-id="e62bb-111">Пример 1: назначение именованного контекста</span><span class="sxs-lookup"><span data-stu-id="e62bb-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="e62bb-112">Назначение будущих командлетов PowerShell для Azure для учетной записи, клиента и подписки в контексте "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="e62bb-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="e62bb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e62bb-113">PARAMETERS</span></span>

### <span data-ttu-id="e62bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62bb-114">-DefaultProfile</span></span>
<span data-ttu-id="e62bb-115">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e62bb-115">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62bb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e62bb-116">-InputObject</span></span>
<span data-ttu-id="e62bb-117">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e62bb-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: SelectByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e62bb-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e62bb-118">-Name</span></span>
<span data-ttu-id="e62bb-119">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="e62bb-119">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: SelectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62bb-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="e62bb-120">-Scope</span></span>
<span data-ttu-id="e62bb-121">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="e62bb-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62bb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e62bb-122">-Confirm</span></span>
<span data-ttu-id="e62bb-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e62bb-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62bb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62bb-124">-WhatIf</span></span>
<span data-ttu-id="e62bb-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e62bb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62bb-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e62bb-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62bb-127">CommonParameters</span></span>
<span data-ttu-id="e62bb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e62bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62bb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62bb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62bb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e62bb-130">INPUTS</span></span>

### <span data-ttu-id="e62bb-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="e62bb-131">None</span></span>

## <span data-ttu-id="e62bb-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e62bb-132">OUTPUTS</span></span>

### <span data-ttu-id="e62bb-133">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e62bb-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="e62bb-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e62bb-134">NOTES</span></span>

## <span data-ttu-id="e62bb-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e62bb-135">RELATED LINKS</span></span>

