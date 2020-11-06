---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 0e102d6c0c4db5bd3d93d4349a2a0e06284cd8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564131"
---
# <span data-ttu-id="6286c-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6286c-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="6286c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6286c-102">SYNOPSIS</span></span>
<span data-ttu-id="6286c-103">Удаление контекста из набора доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="6286c-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6286c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6286c-104">SYNTAX</span></span>

### <span data-ttu-id="6286c-105">RemoveByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6286c-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6286c-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="6286c-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="6286c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6286c-107">DESCRIPTION</span></span>
<span data-ttu-id="6286c-108">Удаление контекста Azure из набора контекстов</span><span class="sxs-lookup"><span data-stu-id="6286c-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="6286c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6286c-109">EXAMPLES</span></span>

### <span data-ttu-id="6286c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6286c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="6286c-111">Удалить контекст с именем по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6286c-111">Remove the context named default</span></span>

## <span data-ttu-id="6286c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6286c-112">PARAMETERS</span></span>

### <span data-ttu-id="6286c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6286c-113">-DefaultProfile</span></span>
<span data-ttu-id="6286c-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6286c-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6286c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6286c-115">-Force</span></span>
<span data-ttu-id="6286c-116">Удалить контекст даже в том случае, если это defualt</span><span class="sxs-lookup"><span data-stu-id="6286c-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="6286c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6286c-117">-InputObject</span></span>
<span data-ttu-id="6286c-118">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6286c-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6286c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6286c-119">-Name</span></span>
<span data-ttu-id="6286c-120">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="6286c-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6286c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6286c-121">-PassThru</span></span>
<span data-ttu-id="6286c-122">Вернуть удаленный контекст</span><span class="sxs-lookup"><span data-stu-id="6286c-122">Return the removed context</span></span>

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

### <span data-ttu-id="6286c-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="6286c-123">-Scope</span></span>
<span data-ttu-id="6286c-124">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="6286c-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="6286c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6286c-125">-Confirm</span></span>
<span data-ttu-id="6286c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6286c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6286c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6286c-127">-WhatIf</span></span>
<span data-ttu-id="6286c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6286c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6286c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6286c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6286c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6286c-130">CommonParameters</span></span>
<span data-ttu-id="6286c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6286c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6286c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6286c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6286c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6286c-133">INPUTS</span></span>

### <span data-ttu-id="6286c-134">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6286c-134">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="6286c-135">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6286c-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6286c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6286c-136">OUTPUTS</span></span>

### <span data-ttu-id="6286c-137">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6286c-137">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="6286c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6286c-138">NOTES</span></span>

## <span data-ttu-id="6286c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6286c-139">RELATED LINKS</span></span>
